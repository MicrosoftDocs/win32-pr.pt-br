---
title: Estruturas flexíveis de EAPHost
description: Saiba mais sobre as estruturas de API flexíveis EAPHost, como EAP \_ CRED REQ e \_ EAP \_ METHOD PROPERTY \_ \_ ARRAY.
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904613"
---
# <a name="eaphost-supplicant-structures"></a>Estruturas flexíveis de EAPHost

As estruturas de API flexíveis EAPHost são as a seguir.



| Estrutura                                                                        | Descrição                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                           | Contém as credenciais EAP novas e antigas para operações de alteração de credencial.                                    |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                         | Contém as credenciais EAP novas e antigas para operações de alteração de credencial.                                    |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contém as credenciais de EAP novas e antigas para operações de expiração de credencial                                     |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contém as credenciais de EAP novas e antigas para operações de expiração de credencial.                                    |
| [**EAP \_ CRED \_ LOGON \_ REQ**](eap-cred-logon-req.md)                              | Contém credenciais de EAP para autenticação de rede.                                                                 |
| [**EAP \_ CRED \_ LOGON \_ RESP**](eap-cred-logon-resp.md)                            | Contém credenciais de EAP para autenticação de rede.                                                                 |
| [**DADOS \_ \_ INTERATIVOS DA INTERFACE DO USUÁRIO DO EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contém informações de configuração para componentes interativos da interface do usuário gerados em um suplente de EAP.            |
| [**PROPRIEDADE DE \_ MÉTODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 ou posterior: representa uma propriedade de método.                                                                    |
| [**MATRIZ DE PROPRIEDADES \_ \_ DO MÉTODO EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 ou posterior: contém uma matriz de estruturas de propriedade de método.                                                 |
| [**VALOR DA PROPRIEDADE DO MÉTODO EAP \_ \_ \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 ou posterior: contém um valor da propriedade de método.                                                                |
| [**VALOR DA PROPRIEDADE DO MÉTODO EAP \_ \_ \_ \_ BOOL**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 ou posterior: contém um valor da propriedade do método de tipo de dados BOOL.                                                 |
| [**VALOR DA PROPRIEDADE DO MÉTODO EAP \_ \_ \_ \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 ou posterior: contém um valor da propriedade do método de tipo de dados DWORD.                                                |
| [**CADEIA DE CARACTERES DE VALOR \_ \_ DA PROPRIEDADE DO MÉTODO \_ EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 ou posterior: contém um valor da propriedade do método de tipo de dados string.                                               |
| [**INFORMAÇÕES DE \_ AUTH DO EAPHOST \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Descreve as informações de autenticação atuais em diferentes estágios do processo de autenticação de EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contém os dados de resultado gerados pelo EAPHost durante uma sessão de autenticação que é passada para um método EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 ou posterior: contém as informações de NAP (Proteção de Acesso à Rede) em um suplente de EAP.                   |



 

 

 