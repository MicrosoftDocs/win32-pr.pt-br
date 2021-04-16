---
description: Lista as estruturas usadas com APIs de gerenciamento de segurança.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Estruturas de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758266"
---
# <a name="security-management-structures"></a>Estruturas de gerenciamento de segurança

Esta seção contém páginas de referência para os seguintes grupos de estruturas:

-   [Estruturas de gerenciamento de política LSA](#lsa-policy-management-structures)
-   [Estruturas de anexo](#attachment-structures)
-   [Estruturas mais seguras](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Estruturas de gerenciamento de política LSA

As estruturas a seguir são usadas pelas funções de gerenciamento de política de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA).



| Estrutura                                                                       | Descrição                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informações de autenticação LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Contém informações de autenticação para um domínio confiável.                                                                                     |
| [**\_informações de enumeração de LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Contém um ponteiro para um [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**\_atributos do objeto LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Especifica os atributos de uma conexão com o objeto de [**política**](policy-object.md) .                                                       |
| [**\_lista de \_ domínios REFERENCIAdos LSA \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Contém informações sobre os domínios referenciados em uma operação de pesquisa.                                                                      |
| [**\_nome traduzido da LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Contém informações sobre a conta identificada por um SID.                                                                                   |
| [**\_Sid traduzido LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Contém informações sobre o SID que identifica uma conta.                                                                                |
| [**\_SID2 traduzido LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Contém informações sobre o SID que identifica uma conta.                                                                                |
| [**\_informações de confiança LSA \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifica um domínio.                                                                                                                          |
| [**Cadeia de caracteres do LSA \_ Unicode \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Contém uma cadeia de caracteres e suas informações de comprimento.                                                                                                 |
| [**\_informações de \_ domínio da conta de política \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Usado para definir e consultar o nome e o SID do domínio da conta do sistema.                                                                        |
| [**\_informações de \_ eventos de auditoria de política \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Usado para definir e consultar as regras de auditoria do sistema.                                                                                            |
| [**\_informações de \_ domínio \_ DNS da política**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Usado para definir e consultar informações de DNS (sistema de nomes de domínio) sobre o domínio primário associado a um objeto de [**política**](policy-object.md) . |
| [**\_informações da \_ função de servidor LSA \_ da política \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Usado para definir e consultar a função de um servidor LSA.                                                                                              |
| [**\_informações de modificação de política \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Usado para consultar informações sobre a hora de criação e a última modificação do banco de dados LSA.                                                  |
| [**\_informações da \_ conta \_ PD da política**](policy-pd-account-info.md)                     | Obsoleto. As estações de trabalho usam o nome da estação de trabalho seguido por um $ como o nome da conta.                                                          |
| [**\_informações de \_ domínio \_ primário da política**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Obsoleto. Em vez disso, use **PolicyDnsDomainInformation** e a estrutura de [**\_ \_ \_ informações de domínio DNS da política**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) .           |
| [**\_informações de \_ autenticação de domínio confiável \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Usado para recuperar informações de autenticação para um domínio confiável.                                                                             |
| [**\_ \_ informações completas do domínio confiável \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Usado para recuperar informações completas sobre um domínio confiável.                                                                                 |
| [**\_ \_ informações básicas de domínio confiável \_**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Informações sobre um domínio confiável. Essa estrutura é idêntica às [**\_ \_ informações de confiança da LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**\_informações de domínio confiável \_ \_ ex.**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Usado para recuperar informações estendidas sobre um domínio confiável.                                                                                 |
| [**\_informações de \_ nome de domínio confiável \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Usado para consultar ou definir o nome de um domínio confiável.                                                                                            |
| [**\_informações de senha confiável \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Usado para consultar ou definir a senha de um domínio confiável.                                                                                       |
| [**\_informações de \_ deslocamento \_ POSIX confiáveis**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Usado para consultar ou definir o valor usado para gerar identificadores de usuário e grupo POSIX.                                                             |



 

Os seguintes tipos de estrutura são obsoletos ou são reservados para uso futuro:

-   **\_informações de \_ \_ consulta completa de auditoria \_ de política**
-   **\_informações do \_ \_ conjunto completo de auditoria \_ de política**
-   **\_informações do \_ log de auditoria de política \_**
-   **\_informações de \_ cota \_ padrão da política**
-   **\_informações de \_ origem da réplica de política \_**
-   **\_informações de controladores confiáveis \_**

## <a name="attachment-structures"></a>Estruturas de anexo

As estruturas a seguir são usadas pelas DLLs de anexo de configuração de segurança e suas funções de suporte. Essas estruturas são definidas em Scesvc. h.



| Estrutura                                                        | Descrição                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informações de configuração do SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Contém informações de configuração para um serviço.                                                                                               |
| [**\_linha de configuração do SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Contém informações sobre uma linha de dados de configuração.                                                                                        |
| [**\_informações de análise de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Contém as informações de análise.                                                                                                              |
| [**\_linha de análise de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Contém a chave, o valor e o comprimento do valor para uma linha específica especificada por uma estrutura de [**\_ \_ informações de análise de SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) . |
| [**informações de retorno de chamada do SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Contém um identificador de banco de dados opaco e ponteiros de função de retorno de chamada para consultar, definir e informações gratuitas.                                          |



 

## <a name="safer-structures"></a>Estruturas mais seguras

As seguintes estruturas e tipos enumerados são usados com mais segurança. Eles são definidos em WinSafer. h.



| Estrutura                                                                | Descrição                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedades do \_ código mais seguro \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Contém informações de imagem de código e critérios a serem verificados na imagem de código. Uma matriz dessas estruturas é passada para a função [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) .                                                                  |
| [**cabeçalho de \_ identificação mais seguro \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Estrutura de cabeçalho para [**\_ \_ identificação de nome de caminho mais segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), [**\_ \_ identificação de hash mais segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)e estruturas de [**\_ \_ identificação de UrlZone mais seguras**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) . |
| [**identificação do \_ nome do caminho mais seguro \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Contém o nome do caminho de uma imagem de código a ser verificada.                                                                                                                                                                                                      |
| [**identificação de \_ hash mais segura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifica um hash da imagem de código a ser verificada.                                                                                                                                                                                                      |
| [**identificação de \_ UrlZone mais segura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Identifica a zona de URL da origem da imagem de código a ser verificada.                                                                                                                                                                                      |



 

 

 
