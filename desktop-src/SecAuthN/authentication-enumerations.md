---
description: Lista as enumerações usadas em APIs de autenticação.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumerações de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc42553074b79726c9d1b70bfc6292f4acf44df225fa1f86c7f7a28289ec8ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101316"
---
# <a name="authentication-enumerations"></a>Enumerações de autenticação

As enumerações de autenticação são categorizadas de acordo com o uso da seguinte forma:

-   [Enumerações de gerenciamento de credenciais](#credentials-management-enumerations)
-   [Enumerações LSA](#lsa-enumerations)
-   [Enumerações do provedor de rede](#network-provider-enumerations)
-   [Enumerações credSSP (provedor de suporte de segurança de credencial)](#credential-security-support-provider-credssp-enumerations)
-   [Outras enumerações](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerações de gerenciamento de credenciais

O Gerenciamento de Credenciais usa as enumerações a seguir.



| Enumeração                                            | Descrição                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ MARSHAL \_ CRED**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contém os tipos de credencial que podem ser marshalados por [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) ou desmarque por [**CredUnmarshalCredential.**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)<br/> |
| [**TIPO DE \_ PROTEÇÃO \_ CRED**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Especifica o contexto de segurança no qual as credenciais são criptografadas ao usar a [**função CredProtect.**](/windows/desktop/api/WinCred/nf-wincred-credprotecta)<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumerações LSA

O LSA usa as enumerações a seguir.



| Enumeração                                                                                   | Descrição                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE ENVIO \_ DE LOGON \_ \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Lista o tipo de logon que está sendo solicitado.<br/>                                                                                                                                                                                                                  |
| [**TIPO DE BUFFER DE PERFIL KERB \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Lista o tipo de perfil de logon retornado.<br/>                                                                                                                                                                                                                 |
| [**TIPO DE MENSAGEM DE PROTOCOLO KERB \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Lista os tipos de mensagens que podem ser enviadas para o pacote de autenticação [*Kerberos*](/windows/desktop/SecGloss/k-gly) chamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**TIPO DE REGISTRO DE COLISÃO DE \_ \_ CONFIANÇA \_ DA \_ \_ FLORESTA LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Define os tipos de colisão que podem ocorrer entre registros de confiança da floresta LSA.<br/>                                                                                                                                                                           |
| [**TIPO DE REGISTRO DE CONFIANÇA DA FLORESTA LSA \_ \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Define o tipo de um registro de confiança de floresta LSA.<br/>                                                                                                                                                                                                           |
| [**TIPO DE INFORMAÇÕES DO TOKEN LSA \_ \_ \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Especifica os níveis de informações que podem ser incluídas em um token de logon.<br/>                                                                                                                                                                                |
| [**TIPO DE ENVIO DE LOGON MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Lista o tipo de logon que está sendo solicitado.<br/>                                                                                                                                                                                                                  |
| [**TIPO DE BUFFER DE PERFIL MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Lista o tipo de perfil de logon retornado.<br/>                                                                                                                                                                                                                 |
| [**TIPO DE MENSAGEM DE PROTOCOLO MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Lista os tipos de mensagens que podem ser enviadas para o Pacote de Autenticação [MSV1 \_ 0](msv1-0-authentication-package.md) chamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**CLASSE DE \_ INFORMAÇÕES DE DOMÍNIO DE \_ \_ POLÍTICA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Define o tipo de informações de domínio da política.<br/>                                                                                                                                                                                                            |
| [**TIPO \_ DE LOGON \_ DE SEGURANÇA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica o tipo de logon solicitado por um processo de logon.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumerações do provedor de rede

O Provedor de Rede usa as enumerações a seguir.



| Enumeração                                                                       | Descrição                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CLASSE DE INFORMAÇÕES ESTENDIDAS SECPKG \_ \_ \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo de enumeração que especifica o tipo de informações a definir ou obter para um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**TIPO DE NOME \_ SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valor de enumeração que especifica o tipo de nome especificado para uma conta.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumerações credSSP (provedor de suporte de segurança de credencial)

CredSSP usa as enumerações a seguir.



| Enumeração                                          | Descrição                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ ENVIO \_ CREDSPP**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Especifica o tipo de credenciais especificado por uma [**estrutura CREDSSP \_ CRED.**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred)<br/> |



 

## <a name="other-enumerations"></a>Outras enumerações

Aqui estão as outras enumerações usadas pela Autenticação.



| Enumeração                                                   | Descrição                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ IDENTIDADE**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Especifica o tipo de identidades a enumerar.<br/>                                                                                                                                                                  |
| [**TIPO DE ENVIO DE LOGON PKU2U \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica o tipo de mensagem de logon passada em uma estrutura LOGON de [**\_ CERTIFICADO \_ S4U PKU2U. \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon)<br/>                                                                                |
| [**STATUS DE \_ SECPKG ATTR \_ LCT \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica se o token da chamada mais recente para a [**função InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) é o último token do cliente.<br/>                               |
| [**CLASSE CRED SECPKG \_ \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica o tipo de credencial usado em um contexto de cliente. A [**enumeração SECPKG \_ CRED \_ CLASS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) é usada na estrutura [**SecPkgContext \_ CredInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo)<br/> |



 

 

