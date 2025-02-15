<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->
<!-- # - version : zrfisaac.wiki.es.mssql : 0.0.2 -->

<!-- # [ markdown ] -->
# SQL Server

## Descripción
SQL Server es un sistema de gestión de bases de datos relacionales (RDBMS) desarrollado por Microsoft, diseñado para almacenar, recuperar y gestionar datos. Soporta una amplia gama de aplicaciones, desde proyectos a pequeña escala hasta grandes sistemas empresariales. SQL Server ofrece características robustas como consultas avanzadas, análisis, seguridad e integración con herramientas de Microsoft, lo que lo convierte en una solución potente para aplicaciones basadas en datos.

---

## Índice
- Predeterminado
  - Puerto : `1433` `5920`
  - Usuario : `sa`
  - Base de datos : `master`
- Descargas
  - Controlador ODBC para SQL Server :
      [`18-aarch64`](https://go.microsoft.com/fwlink/?linkid=2281322)
      [`18-amd64`](https://go.microsoft.com/fwlink/?linkid=2280794)
      [`18-i386`](https://go.microsoft.com/fwlink/?linkid=2281260)
      [`17-amd64`](https://go.microsoft.com/fwlink/?linkid=2266337)
      [`17-i386`](https://go.microsoft.com/fwlink/?linkid=2266446)
  - OLE DB para SQL Server :
      [`19-aarch64`](https://go.microsoft.com/fwlink/?linkid=2277846)
      [`19-amd64`](https://go.microsoft.com/fwlink/?linkid=2278038)
      [`19-i386`](https://go.microsoft.com/fwlink/?linkid=2278037)
  - SQL Server Developer :
      [`2022`](https://download.microsoft.com/download/c/c/9/cc9c6797-383c-4b24-8920-dc057c1de9d3/SQL2022-SSEI-Dev.exe)
      [`2019`](https://go.microsoft.com/fwlink/?linkid=866662)
  - SQL Server Management Studio :
      [`setup`](https://aka.ms/ssmsfullsetup)
- [Ejemplo](#ejemplo)
  - Columna
  - Base de datos
  - Función
  - [Procedimiento](#procedimiento)
  - [Tabla](#tabla)
  - Usuario
  - Vista

---

## [Ejemplo](#índice)

### [Procedimiento](#índice)

```sql
IF  EXISTS (
  SELECT TOP 1 NULL
  FROM SYSOBJECTS WITH(NOLOCK)
  WHERE XTYPE = N'P'
  AND NAME = N'PR_DEBUG'
) DROP PROCEDURE PR_DEBUG
GO
CREATE PROCEDURE PR_DEBUG
  @P_DATA VARCHAR(32)
AS
  SELECT @P_DATA AS P_DEBUG
GO
EXEC PR_DEBUG @P_DATA = 'DEBUG'
```

### [Tabla](https://www.google.com/url?sa=E&source=gmail&q=#índice)

```sql
IF NOT EXISTS (
  SELECT TOP 1 NULL
  FROM INFORMATION_SCHEMA.TABLES WITH(NOLOCK)
  WHERE INFORMATION_SCHEMA.TABLES.TABLE_TYPE = N'BASE TABLE'
  AND INFORMATION_SCHEMA.TABLES.TABLE_NAME = N'TB_DEBUG'
)
BEGIN
  CREATE TABLE TB_DEBUG (
     CL_ID         INT  IDENTITY(1, 1) NOT NULL
    ,CL_DEBUG      INT                 NOT NULL
    ,CL_NAME       VARCHAR     ( 400)  NOT NULL
    ,CL_STATUS     VARCHAR     (   1)  NOT NULL
    CONSTRAINT CT_DF_TB_DEBUG_CL_STATUS
    DEFAULT('N')
    -- CONSTRAINT
    ,CONSTRAINT CT_CK_TB_DEBUG_CL_STATUS
    CHECK(CL_STATUS  IN ('Y','N'))
    -- PRIMARY KEY
    ,CONSTRAINT PK_TB_DEBUG_CL_ID
    PRIMARY KEY (CL_ID)
    -- FOREIGN KEY
    ,CONSTRAINT FK_TB_DEBUG_CL_DEBUG
    FOREIGN KEY (CL_DEBUG)
    REFERENCES TB_DEBUG(CL_ID)
  )
END
```
