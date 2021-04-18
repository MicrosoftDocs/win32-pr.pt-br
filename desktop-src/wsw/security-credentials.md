---
title: Credenciais de Segurança
description: As credenciais de segurança são uma parte da evidência que uma parte de comunicação possui que pode ser usada para criar ou obter um token de segurança.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Serviços Web de credenciais de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105791498"
---
# <a name="security-credentials"></a>Credenciais de Segurança

As credenciais de segurança são uma parte da evidência que uma parte de comunicação possui que pode ser usada para criar ou obter um token de segurança. Assim, as credenciais normalmente são mais longas do que os tokens de segurança, e um token de segurança pode ser exibido como a manifestação de tempo de execução das credenciais de segurança. Exemplos de credenciais incluem um certificado de computador (que pode ser convertido em um token de segurança X. 509 em tempo de execução) ou um par de nome de usuário/senha para um domínio (que pode ser usado para obter um token de segurança Kerberos).


As credenciais são especificadas como parte das [associações de segurança](security-bindings.md).

Os seguintes elementos de API são usados com credenciais de segurança.

| Callback                                                                  | Descrição                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**\_retorno de chamada WS get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Fornece um certificado para o tempo de execução de segurança.          |
| [**\_retorno de \_ chamada de senha do WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Valida um par de nome de usuário/senha no lado do destinatário. |



 



| Enumeração                                                                                           | Descrição                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**\_tipo de \_ credencial WS CERT \_**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | O tipo da credencial do certificado.                       |
| [**\_tipo de \_ credencial WS username \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | O tipo de credencial de nome de usuário/senha.                 |
| [**\_tipo de \_ \_ \_ credencial de \_ autenticação integrada do Windows WS**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | O tipo da credencial de autenticação integrada do Windows. |



 



| Estrutura                                                                                                   | Descrição                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ credencial WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | O tipo base abstrato para todos os tipos de credencial de certificado.                                                          |
| [**\_ \_ credencial de certificado personalizado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | O tipo para especificar uma credencial de certificado que deve ser fornecida por um retorno de chamada para o aplicativo.             |
| [**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS padrão \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Tipo para fornecer uma credencial de autenticação integrada do Windows com base no token de thread atual.                  |
| [**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS opaca \_**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Digite para fornecer uma credencial de autenticação integrada do Windows.                                                    |
| [**\_ \_ credencial de nome de usuário WS String \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | O tipo para fornecer um par de nome de usuário/senha como cadeias de caracteres.                                                           |
| [**\_ \_ \_ \_ credencial de autenticação integrada do Windows WS String \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Digite para fornecer uma credencial do Windows como nome de usuário, senha e cadeias de caracteres de domínio.                                        |
| [**\_ \_ \_ credencial de certificado do nome da entidade WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | O tipo para especificar uma credencial de certificado usando o nome da entidade do certificado, o local do repositório e o nome do repositório. |
| [**\_ \_ credencial de certificado de impressão digital WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | O tipo para especificar uma credencial de certificado usando a impressão digital do certificado, o local do repositório e o nome do repositório.   |
| [**\_ \_ credencial WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | O tipo base abstrato para todas as credenciais de nome de usuário/senha.                                                         |
| [**\_ \_ \_ credencial de autenticação \_ integrada do Windows WS**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | O tipo base abstrato para todos os tipos de credenciais usados com a autenticação integrada do Windows.                          |



 

 

 




