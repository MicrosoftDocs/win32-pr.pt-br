---
title: Estruturas comuns de API do EAPHost
description: Saiba mais sobre estruturas comuns de API do EAPHost. Consulte uma lista de estruturas usadas por todas as tecnologias EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4740658f798eadee2a658df1a7f9f8fd44b386c4ac39b52bcf49e75887d2d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984326"
---
# <a name="common-eaphost-api-structures"></a>Estruturas comuns de API do EAPHost

A tabela a seguir lista as estruturas que são comuns a todas as tecnologias de API do EAPHost.



| Estrutura                                                                | Descrição                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contém um atributo EAP.                                                                                                                                                                                              |
| [**ATRIBUTOS \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contém uma matriz de atributos EAP.                                                                                                                                                                                    |
| [**MATRIZ DE CAMPOS \_ DE \_ ENTRADA DE \_ CONFIGURAÇÃO DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contém um conjunto de estruturas de DADOS DE CAMPO DE ENTRADA DE CONFIGURAÇÃO DE EAP que contêm coletivamente os dados de campo de entrada do usuário obtidos de uma caixa de diálogo de configuração de SSO (logout único) do EAP. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) |
| [**DADOS DO CAMPO \_ DE ENTRADA DE \_ \_ CONFIGURAÇÃO DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contém os dados associados a um único campo de entrada em uma caixa de diálogo de configuração de SSO (logout único) do EAP.                                                                                                              |
| [**ERRO \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contém dados sobre um erro que ocorreu durante uma operação EAPHost.                                                                                                                                                 |
| [**INFORMAÇÕES DO MÉTODO EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contém dados específicos para um método EAP.                                                                                                                                                                               |
| [**INFORMAÇÕES DO MÉTODO EAP \_ \_ \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista com Service Pack 1 (SP1) ou posterior: contém dados específicos para um método EAP.                                                                                                                             |
| [**MATRIZ DE INFORMAÇÕES DO MÉTODO EAP \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contém informações sobre métodos EAP instalados no computador cliente.                                                                                                                                                   |
| [**MATRIZ DE INFORMAÇÕES DO MÉTODO EAP \_ \_ \_ \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista com SP1 ou posterior: contém informações sobre todos os métodos EAP instalados no computador cliente.                                                                                                    |
| [**TIPO DE MÉTODO EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contém dados de tipo, identificação e autor para um método EAP.                                                                                                                                                       |
| [**TIPO \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contém dados de identificação de tipo e de fornecedor para um método EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contém um pacote de dados opaco enviados durante uma sessão de autenticação de EAP.                                                                                                                                             |



 

 

 




