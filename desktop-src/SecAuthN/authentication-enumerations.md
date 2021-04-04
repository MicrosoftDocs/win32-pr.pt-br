---
description: Lista as enumerações usadas em APIs de autenticação.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumerações de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647008"
---
# <a name="authentication-enumerations"></a>Enumerações de autenticação

As enumerações de autenticação são categorizadas de acordo com o uso da seguinte maneira:

-   [Enumerações de gerenciamento de credenciais](#credentials-management-enumerations)
-   [Enumerações LSA](#lsa-enumerations)
-   [Enumerações de provedor de rede](#network-provider-enumerations)
-   [Enumerações do provedor de suporte à segurança de credenciais (CredSSP)](#credential-security-support-provider-credssp-enumerations)
-   [Outras enumerações](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerações de gerenciamento de credenciais

O gerenciamento de credenciais usa as seguintes enumerações.



| Enumeração                                            | Descrição                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de Marshal de cred \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contém os tipos de credencial que podem ser empacotados por [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) ou não marshaled por [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).<br/> |
| [**\_tipo de proteção de credenciais \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Especifica o contexto de segurança no qual as credenciais são criptografadas ao usar a função [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) .<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumerações LSA

O LSA usa as seguintes enumerações.



| Enumeração                                                                                   | Descrição                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ envio de logon do KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Lista o tipo de logon que está sendo solicitado.<br/>                                                                                                                                                                                                                  |
| [**\_tipo de \_ buffer do perfil KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Lista o tipo de perfil de logon retornado.<br/>                                                                                                                                                                                                                 |
| [**\_tipo de \_ mensagem de protocolo KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Lista os tipos de mensagens que podem ser enviadas para o pacote de autenticação [*Kerberos*](/windows/desktop/SecGloss/k-gly) chamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**\_tipo de \_ registro de colisão de confiança da floresta LSA \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Define os tipos de colisão que podem ocorrer entre registros de confiança de floresta LSA.<br/>                                                                                                                                                                           |
| [**\_tipo de \_ registro de confiança de floresta LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Define o tipo de um registro de confiança de floresta LSA.<br/>                                                                                                                                                                                                           |
| [**\_tipo de \_ informação do token LSA \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Especifica os níveis de informações que podem ser incluídos em um token de logon.<br/>                                                                                                                                                                                |
| [**\_Tipo de \_ envio de logon \_ \_ do MSV1 0**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Lista o tipo de logon que está sendo solicitado.<br/>                                                                                                                                                                                                                  |
| [**\_Tipo de \_ buffer de perfil MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Lista o tipo de perfil de logon retornado.<br/>                                                                                                                                                                                                                 |
| [**\_Tipo de \_ mensagem de protocolo MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Lista os tipos de mensagens que podem ser enviadas para o [ \_ pacote de autenticação MSV1 0](msv1-0-authentication-package.md) chamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**\_classe de \_ informações de domínio de política \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Define o tipo de informações de domínio de política.<br/>                                                                                                                                                                                                            |
| [**\_tipo de logon de segurança \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica o tipo de logon solicitado por um processo de logon.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumerações de provedor de rede

O provedor de rede usa as seguintes enumerações.



| Enumeração                                                                       | Descrição                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_classe de \_ informações ESTENDIdas SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo de enumeração que especifica o tipo de informações a serem definidas ou obtidas para um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**\_tipo de nome de SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valor de enumeração que especifica o tipo de nome especificado para uma conta.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumerações do provedor de suporte à segurança de credenciais (CredSSP)

O CredSSP usa as seguintes enumerações.



| Enumeração                                          | Descrição                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_tipo de envio CREDSPP \_**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Especifica o tipo de credenciais especificado por uma estrutura de [**\_ credenciais CREDSSP**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) .<br/> |



 

## <a name="other-enumerations"></a>Outras enumerações

Aqui estão as outras enumerações usadas pela autenticação.



| Enumeração                                                   | Descrição                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de identidade \_**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Especifica o tipo de identidades a serem enumeradas.<br/>                                                                                                                                                                  |
| [**\_Tipo de \_ envio de logon do PKU2U \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica o tipo de mensagem de logon passada em uma estrutura de [**\_ \_ \_ logon S4U de certificado PKU2U**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) .<br/>                                                                                |
| [**SECPKG \_ attr \_ LCT \_ status**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica se o token da chamada mais recente para a função [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) é o último token do cliente.<br/>                               |
| [**\_classe de credenciais SECPKG \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica o tipo de credencial usada em um contexto de cliente. A enumeração de [**\_ \_ classe de credenciais SECPKG**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) é usada na estrutura [**\_ CredInfo SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) .<br/> |



 

 

