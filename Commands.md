


### Objetos dentro de un esquema
```
SELECT
    * 
FROM
    sys.objects 
WHERE
    schema_id = SCHEMA_ID('srec_configuration_manager')
```
#### Tablas que pertenecen a un esquema
```
SELECT
    * 
FROM
    INFORMATION_SCHEMA.TABLES 
WHERE
    TABLE_SCHEMA = 'srec_service_provider_payment_file' 
    and table_type='BASE TABLE' 
```

### Llaves foraneas en una tabla
```
sp_help 'srec_provided_account_service.payment_channel_service'
```

### Obtener información de las columnas de una tabla
```
exec sp_columns 'service', @table_owner ='srec_provided_account_service'
```