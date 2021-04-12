---
title: Estruturas do suplicante EAPHost
description: Saiba mais sobre as estruturas de API suplicante do EAPHost, como EAP \_ cred \_ req e a \_ matriz de propriedades do método EAP \_ \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7121e123fd790a54a95dafb59c080f435ca917
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366700"
---
# <a name="eaphost-supplicant-structures"></a>Estruturas do suplicante EAPHost

As estruturas de API suplicante do EAPHost são as seguintes.



| Estrutura                                                                        | Descrição                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Req. de \_ credenciais EAP \_**](eap-cred-req.md)                                           | Contém as credenciais EAP antigas e novas para operações de alteração de credencial.                                    |
| [**\_resp de credenciais EAP \_**](eap-cred-resp.md)                                         | Contém as credenciais EAP antigas e novas para operações de alteração de credencial.                                    |
| [**Req. de \_ expiração de credenciais EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contém as credenciais EAP antigas e novas para operações de expiração de credenciais                                     |
| [**\_resp de \_ expiração de credenciais EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contém as credenciais EAP antigas e novas para as operações de expiração de uma credencial.                                    |
| [**Req. de \_ logon de credenciais EAP \_ \_**](eap-cred-logon-req.md)                              | Contém credenciais EAP para autenticação de rede.                                                                 |
| [**\_resp de \_ logon de credenciais EAP \_**](eap-cred-logon-resp.md)                            | Contém credenciais EAP para autenticação de rede.                                                                 |
| [**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contém informações de configuração para componentes interativos da interface do usuário gerados em um suplicante EAP.            |
| [**\_Propriedade do método EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 ou posterior: representa uma propriedade de método.                                                                    |
| [**\_matriz de \_ Propriedades do método EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 ou posterior: contém uma matriz de estruturas de propriedades de método.                                                 |
| [**\_valor da \_ Propriedade do método EAP \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 ou posterior: contém um valor de propriedade de método.                                                                |
| [**\_valor da Propriedade do método EAP \_ \_ \_ bool**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 ou posterior: contém um valor de propriedade de método de tipo de dados BOOL.                                                 |
| [**\_valor da Propriedade do método EAP \_ \_ \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 ou posterior: contém um valor de propriedade de método de tipo de dados DWORD.                                                |
| [**\_cadeia de \_ caracteres do valor da Propriedade do método EAP \_ \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 ou posterior: contém um valor de propriedade de método de tipo de dados de cadeia de caracteres.                                               |
| [**\_informações de autenticação do EAPHost \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Descreve as informações de autenticação atuais em diferentes estágios do processo de autenticação EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contém os dados de resultado gerados pelo EAPHost durante uma sessão de autenticação que é passada para um método EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 ou posterior: contém as informações de NAP (proteção de acesso à rede) em um suplicante de EAP.                   |



 

 

 