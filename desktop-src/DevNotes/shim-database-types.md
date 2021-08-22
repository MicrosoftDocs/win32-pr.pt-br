---
description: Representar os tipos para bancos de dados de shim personalizados e principais.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipos de banco de dados shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075920"
---
# <a name="shim-database-types"></a>Tipos de banco de dados shim

Representar os tipos para bancos de dados de shim personalizados e principais.



| Constante/valor                                                                                                                                                                                                                                                | Descrição                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ BANCO \_ DE DADOS PRINCIPAL**</dt> <dt>0x80000000</dt> </dl>                    | O banco de dados principal. Se esse sinalizador não estiver presente, o banco de dados será um banco de dados personalizado.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ BANCO \_ DE DADOS SHIM**</dt> <dt>0x00010000</dt> </dl>                    | O banco de dados contém entradas de aplicativo a serem shimed.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ Banco \_ de Dados MSI**</dt> <dt>0x00020000</dt> </dl>                       | O banco de dados contém entradas MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ DRIVERS DE \_ BANCO**</dt> <dt>DE DADOS 0x00040000</dt> </dl>           | O banco de dados contém entradas de bloco de driver.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ DETALHES \_ DO BANCO DE**</dt> <dt>0X00080000</dt> </dl>           | O banco de dados contém detalhes do Apphelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ DETALHES \_ DO BANCO \_ DE**</dt> <dt>DADOS SP 0x00100000</dt> </dl> | O banco de dados contém detalhes do SP Apphelp.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ BANCO \_ DE DADOS RESOURCE**</dt> <dt>0x00200000</dt> </dl>        | A DLL do recurso contém detalhes do Apphelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ MÁSCARA \_ DE TIPO DE BANCO \_ DE**</dt> <dt>DADOS 0XF02F0000</dt> </dl>    | Uma máscara usada para extrair informações principais do banco de dados.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SHIM PRINCIPAL DO \_ BANCO \_ DE DADOS \_ SDB**</dt> </dl>                                                                    | BANCO DE DADOS SDB \_ \_ SHIM \| SDB BANCO DE DADOS \_ \_ MSI \| SDB \_ \_ PRINCIPAL<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**\_MSI PRINCIPAL DO BANCO DE DADOS \_ \_ SDB**</dt> </dl>                                                                       | BANCO DE \_ DADOS \_ SDB MSI \| SDB \_ PRINCIPAL \_<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**DRIVERS PRINCIPAIS DO \_ BANCO \_ DE DADOS \_ SDB**</dt> </dl>                                                           | SDB \_ DATABASE \_ DRIVERS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**DETALHES PRINCIPAIS DO \_ BANCO DE \_ DADOS SDB \_**</dt> </dl>                                                           | SDB \_ DATABASE \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**DETALHES DO \_ SP PRINCIPAL DO BANCO DE DADOS \_ \_ \_ SDB**</dt> </dl>                                                 | SDB \_ DATABASE \_ SP \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**RECURSO PRINCIPAL \_ DO BANCO DE DADOS \_ \_ SDB**</dt> </dl>                                                        | SDB \_ DATABASE \_ RESOURCE \| SDB \_ DATABASE \_ MAIN<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




