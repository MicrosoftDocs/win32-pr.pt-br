---
title: Estruturas comuns de API do EAPHost
description: Saiba mais sobre estruturas comuns de API do EAPHost. Consulte uma lista de estruturas usadas por todas as tecnologias EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641871"
---
# <a name="common-eaphost-api-structures"></a>Estruturas comuns de API do EAPHost

A tabela a seguir lista as estruturas que são comuns a todas as tecnologias de API do EAPHost.



| Estrutura                                                                | Descrição                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contém um atributo EAP.                                                                                                                                                                                              |
| [**atributos de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contém uma matriz de atributos EAP.                                                                                                                                                                                    |
| [**\_matriz de \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contém um conjunto de estruturas de [**dados de campo de \_ entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) que contêm coletivamente os dados de campo de entrada do usuário obtidos de uma caixa de diálogo de configuração de SSO (logon único) EAP. |
| [**\_dados do \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contém os dados associados a um único campo de entrada em uma caixa de diálogo de configuração de logon único (SSO) EAP.                                                                                                              |
| [**erro de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contém dados sobre um erro que ocorreu durante uma operação EAPHost.                                                                                                                                                 |
| [**\_informações do método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contém dados específicos para um método EAP.                                                                                                                                                                               |
| [**\_informações do método EAP \_ \_ ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista com Service Pack 1 (SP1) ou posterior: contém dados específicos para um método EAP.                                                                                                                             |
| [**\_matriz de \_ informações do método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contém informações sobre os métodos EAP instalados no computador cliente.                                                                                                                                                   |
| [**\_matriz de informações do método EAP \_ \_ \_ ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista com SP1 ou posterior: contém informações sobre todos os métodos EAP instalados no computador cliente.                                                                                                    |
| [**\_tipo de método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contém dados de tipo, identificação e autor para um método EAP.                                                                                                                                                       |
| [**tipo de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contém dados de identificação de tipo e fornecedor para um método EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contém um pacote de dados opacos enviados durante uma sessão de autenticação EAP.                                                                                                                                             |



 

 

 




