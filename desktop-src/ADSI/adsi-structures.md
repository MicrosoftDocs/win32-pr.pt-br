---
title: Estruturas ADSI
description: As interfaces de serviço Active Directory (ADSI) definem e usam as estruturas listadas na tabela a seguir.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI, referência, estruturas ADSI
- ADSI de estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f35ba74f0334e8b66329d8f526266c315056af9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084011"
---
# <a name="adsi-structures"></a>Estruturas ADSI

As interfaces de serviço Active Directory (ADSI) definem e usam as estruturas listadas na tabela a seguir.



| Estrutura                                                                      | Descrição                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DEF. de atributo de anúncios \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Descreve um conjunto de definições de atributo de um objeto **attributeSchema** .<br/>                          |
| [**\_informações de attr ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Mantém o valor de um atributo nomeado e especifica operações para modificar o atributo.<br/>              |
| [**\_BACKLINK ADS**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Representa uma representação ADSI do atributo **back link** .<br/>                                   |
| [**\_lista de CASEIGNORE de anúncios \_**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Representa uma representação ADSI do atributo de **lista de Ignorar maiúsculas e minúsculas** .<br/>                            |
| [**DEF. de \_ classe ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Descreve dados de esquema para um objeto.<br/>                                                                |
| [**ADS \_ DN \_ com \_ binário**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Uma estrutura definida por ADSI que mapeia um nome distinto para um **GUID** de objeto.<br/>                     |
| [**\_DN ADS \_ com \_ cadeia de caracteres**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Uma estrutura definida por ADSI que mapeia um nome distinto de um objeto para um valor de cadeia de caracteres que não varie.<br/> |
| [**EMAIL do ADS \_**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Representa uma representação ADSI do atributo **email** .<br/>                                       |
| [**\_FAXNUMBER ADS**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Representa uma representação ADSI do atributo de **número de telefone do fax** .<br/>                  |
| [**isenções de anúncios \_**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Representa uma representação ADSI do atributo **Hold** .<br/>                                        |
| [**Endereço netads \_**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Representa uma representação ADSI do atributo **net address** .<br/>                                 |
| [**\_ \_ descritor de segurança do ADS NT \_**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Descreve um descritor de segurança.<br/>                                                                    |
| [**\_informações do objeto ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Descreve dados de objeto de serviço de diretório.<br/>                                                            |
| [**\_lista de octetos ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Representa uma representação ADSI do atributo de **lista de octetos** .<br/>                                  |
| [**Cadeia de caracteres do \_ OCTETO ADS \_**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Representa uma representação ADSI do atributo de **cadeia de caracteres de octeto** .<br/>                                |
| [**\_caminho ADs**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Representa uma representação ADSI do atributo **path** .<br/>                                        |
| [**\_POSTALADDRESS ADS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Representa uma representação ADSI do atributo de **Endereço postal** .<br/>                              |
| [**AD \_ Prov \_ específico**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Descreve um tipo de dados específico do provedor.<br/>                                                            |
| [**\_REPLICAPOINTER ADS**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Representa uma representação ADSI do atributo de ponteiro de réplica.<br/>                                 |
| [**\_coluna de pesquisa do ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Representa uma coluna resultante de uma consulta de diretório.<br/>                                               |
| [**informações do ADS \_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Descreve as preferências de consulta.<br/>                                                                        |
| [**a \_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Descreve a chave de classificação usada para classificar uma consulta.<br/>                                                    |
| [**\_carimbo de data/hora ADS**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Representa uma representação ADSI do atributo **timestamp** .<br/>                                   |
| [**tipos de anúncios \_**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Representa uma representação ADSI do atributo de **nome tipado** .<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Descreve o valor de um tipo de dados ADSI.<br/>                                                           |
| [**\_VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Especifica que a exibição de lista virtual deve ser usada ao retornar os resultados da pesquisa do servidor.<br/>  |



 

 

 





