---
description: Representa os tipos de bancos de dados de shims principal e personalizado.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipos de banco de dados Shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646193"
---
# <a name="shim-database-types"></a>Tipos de banco de dados Shim

Representa os tipos de bancos de dados de shims principal e personalizado.



| Constante/valor                                                                                                                                                                                                                                                | Descrição                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**Sdb \_ 0x80000000 \_ principal do banco de dados**</dt> <dt></dt> </dl>                    | O banco de dados principal. Se esse sinalizador não estiver presente, o banco de dados será um banco de dados personalizado.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**Sdb \_ 0x00010000 de \_ Shim de banco de dados**</dt> <dt></dt> </dl>                    | O banco de dados contém entradas de aplicativo a serem corrigido.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**Sdb \_ 0x00020000 \_ MSI do banco de dados**</dt> <dt></dt> </dl>                       | O banco de dados contém entradas MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**Sdb \_ \_Drivers de banco de dados**</dt> <dt>0x00040000</dt> </dl>           | O banco de dados contém entradas de bloco de driver.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**Sdb \_ \_Detalhes do banco de dados**</dt> <dt>0x00080000</dt> </dl>           | O banco de dados contém detalhes de AppHelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**Sdb \_ \_ \_ Detalhes do Database SP**</dt> <dt>0x00100000</dt> </dl> | O banco de dados contém os detalhes de AppHelp do SP.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**Sdb \_ 0x00200000 de \_ recurso do banco de dados**</dt> <dt></dt> </dl>        | A DLL de recursos contém detalhes de AppHelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**Sdb \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0xF02F0000</dt> </dl>    | Uma máscara usada para extrair informações do banco de dados principal.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**\_Shim principal do banco de dados sdb \_ \_**</dt> </dl>                                                                    | Banco \_ de dados sdb. \_ \| \_ \_ \| \_ \_<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**\_MSI principal do banco de dados sdb \_ \_**</dt> </dl>                                                                       | banco de dados sdb do MSI do banco de dados SDB \_ \_ \| \_ \_<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_ \_ principais drivers do banco de dados sdb \_**</dt> </dl>                                                           | banco de dados sdb. \_ \_ \| \_ \_<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_detalhes principais do banco de dados sdb \_ \_**</dt> </dl>                                                           | banco de dados sdb detalhes do banco de dados sdb \_ \_ \| \_ \_ principal<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**\_ \_ detalhes principais do SP do banco de dados sdb \_ \_**</dt> </dl>                                                 | \_detalhes do SP do banco de dados sdb banco de \_ \_ \| \_ dados sdb \_ principal<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_recurso principal do banco de dados sdb \_ \_**</dt> </dl>                                                        | \_banco de \_ dados sdb de recurso de banco de dados sdb \| \_ \_ principal<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




