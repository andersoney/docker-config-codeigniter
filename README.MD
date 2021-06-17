### Configuração para corrigir o erro de group by
Na tela de login dá o seguinte erro: 

    which is not functionally dependent on columns in GROUP BY clause; this is incompatible with sql_mode=only_full_group_by

Para corrigir execute o seguinte comando.

    use fase1;
    SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));