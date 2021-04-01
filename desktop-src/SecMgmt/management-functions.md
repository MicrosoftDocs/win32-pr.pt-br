---
description: Lista as funções de suporte fornecidas pelo conjunto de ferramentas de configuração de segurança.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Funções de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829649"
---
# <a name="security-management-functions"></a>Funções de gerenciamento de segurança

Esta seção contém tópicos para os seguintes grupos de funções:

-   [Funções de retorno de chamada de anexo](#attachment-callback-functions)
-   [Funções do mecanismo de anexo](#attachment-engine-functions)
-   [Funções de política LSA](#lsa-policy-functions)
    -   [Funções de política](#lsa-policy-functions)
    -   [Funções de conta](#account-functions)
    -   [Funções de domínio confiável](#trusted-domain-functions)
    -   [Funções de dados particulares](#private-data-functions)
    -   [Funções diversas](#miscellaneous-functions)
-   [Funções de conta de serviço gerenciado](#managed-service-account-functions)
-   [Funções de filtro de senha](#password-filter-functions)
-   [Funções mais seguras](#safer-functions)

## <a name="attachment-callback-functions"></a>Funções de retorno de chamada de anexo

As funções de suporte a seguir são fornecidas pelo conjunto de ferramentas de configuração de segurança e podem ser usadas por mecanismos de anexo e snap-ins de extensão para ler e gravar dados de configuração.



| Função de retorno de chamada                                         | Descrição                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_informações gratuitas do PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Usado para liberar memória alocada por essas funções de suporte.<br/>                        |
| [**\_informações de log do PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Usado para registrar a mensagem no arquivo de log de configuração ou no arquivo de log de análise.<br/>          |
| [**\_informações de consulta do PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Usado para consultar as informações de configuração e análise de um serviço específico.<br/> |
| [**PFSCE \_ definir \_ informações**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Usado para definir informações de configuração e análise para um serviço específico.<br/>       |



 

## <a name="attachment-engine-functions"></a>Funções do mecanismo de anexo



| Função                                                              | Descrição                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Implementado pela DLL do mecanismo de anexo. O mecanismo de configuração de segurança chama essa função quando o sistema é analisado.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Implementado pela DLL do mecanismo de anexo. O mecanismo de configuração de segurança chama essa função quando o sistema é configurado.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Implementado pela DLL do mecanismo de anexo. O mecanismo de configuração de segurança chama essa função quando recebe uma solicitação de atualização de configuração da extensão de snap-in de anexo.<br/> |



 

## <a name="lsa-policy-functions"></a>Funções de política LSA

Os tópicos a seguir fornecem informações de referência para as funções de política de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA).



| Tópico                               | Descrição                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funções de política<br/>         | As funções de detalhes usadas para abrir o objeto de [**política**](policy-object.md) local e para definir ou recuperar informações de política global.<br/>                                                  |
| Funções de conta<br/>        | Funções de detalhes usadas para gerenciar permissões de conta e para criar e excluir contas de usuário.<br/>                                                                                       |
| Funções de domínio confiável<br/> | As funções de detalhes usadas para criar e excluir relações de domínio confiáveis e para definir e recuperar informações sobre esses domínios confiáveis.<br/>                                          |
| Funções de dados particulares<br/>   | Não use as funções de dados particulares de LSA. Em vez disso, use as funções [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .<br/> |
| Funções diversas<br/>  | Funções de detalhes não descritas em outro lugar.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Funções de política

As funções a seguir enumeram contas de usuário e domínios confiáveis, recebem notificações de alteração de política e identificam nomes de conta e SIDs.



| Função                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Enumera todas as contas que têm uma permissão de usuário especificada.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Enumera os domínios confiáveis.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Mapeia os nomes especificados para seus SIDs. Retorna o SID como um par de SID de RID/domínio.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Mapeia os nomes especificados para seus SIDs. Retorna o SID como um único elemento.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Recupera o [*identificador local exclusivo*](/windows/desktop/SecGloss/l-gly) (LUID) usado pela [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) para representar o nome de privilégio especificado.<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Mapeia os nomes de conta especificados para seus SIDs.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registra um objeto de evento para receber notificações quando as informações da política local são alteradas.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Cancela o registro de um objeto de evento que está recebendo notificações de alteração de política.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Funções de conta

As funções a seguir adicionam, enumeram e excluem permissões para uma conta.



| Função                                                                  | Descrição                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Adicione permissões a uma conta. Se a conta ainda não existir, ela será criada.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Enumere as permissões concedidas a uma conta.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Remover permissões de uma conta. Quando todas as permissões forem removidas, a conta será excluída.<br/> |



 

### <a name="trusted-domain-functions"></a>Funções de domínio confiável

As funções a seguir criam, enumeram e excluem domínios confiáveis e definem e recuperam informações de domínio confiável.



| Função                                                                                                                                                    | Descrição                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Cria um novo objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Remove um objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Enumera os domínios atualmente confiáveis pelo sistema local.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Abre um identificador para um objeto [**TrustedDomain**](trusteddomain-object.md) .<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Recupera informações sobre um domínio confiável. O domínio é especificado pelo SID.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Recupera informações sobre um domínio confiável. O domínio é especificado pelo nome.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Define informações para um domínio confiável. O domínio é especificado pelo nome.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Define informações para um domínio confiável. O domínio é especificado pelo SID.<br/>         |



 

### <a name="private-data-functions"></a>Funções de dados particulares

Não use as funções de dados particulares de LSA. Em vez disso, use as funções [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .



| Função                                                            | Descrição                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Recupera e descriptografa uma cadeia de caracteres.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Criptografa e armazena uma cadeia de caracteres.<br/>    |



 

### <a name="miscellaneous-functions"></a>Funções diversas

A API da diretiva LSA tem as três funções a seguir que não se ajustam a nenhuma das outras categorias de função da política LSA.



| Função                                                          | Descrição                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Fecha um identificador para um objeto de [**política**](policy-object.md) ou um objeto [**TrustedDomain**](trusteddomain-object.md) .<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Libera um buffer alocado por uma função LSA.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Converte um valor **NTSTATUS** em um código de erro do Windows.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Funções de conta de serviço gerenciado

As funções a seguir são usadas para criar, enumerar, localizar e excluir contas de serviço gerenciado.



| Função                                                                      | Descrição                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Cria uma conta de serviço gerenciado.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Enumera as contas de servidor no servidor especificado.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Testa se a conta de serviço especificada existe na loja de Netlogon no servidor especificado.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Exclui a conta de serviço especificada do banco de dados [Active Directory](/windows/desktop/AD/active-directory-domain-services) .<br/> |



 

## <a name="password-filter-functions"></a>Funções de filtro de senha

As seguintes funções de [*filtro de senha*](/windows/desktop/SecGloss/p-gly) são implementadas por DLLs de filtro de senha personalizadas para fornecer filtragem de senha e notificação de alteração de senha.



| Função                                                            | Descrição                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Indica que uma DLL de filtro de senha foi inicializada.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Indica que uma senha foi alterada.<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Valida uma nova senha com base na política de senha.<br/>   |



 

## <a name="safer-functions"></a>Funções mais seguras

As funções mais seguras a seguir podem ser usadas para verificar o nível mais seguro de qualquer executável e registrar eventos.



| Função                                                         | Descrição                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Fecha um identificador de \_ nível mais seguro \_ aberto usando a função [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) ou a função [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) .<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Restringe um token usando restrições especificadas por um identificador de \_ nível mais seguro \_ .<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Abre um identificador de \_ nível mais seguro \_ .<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Recupera informações sobre um nível de política.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Recupera informações sobre uma política.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Recupera informações sobre um nível.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Determina se um arquivo especificado é um arquivo executável.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Envia uma mensagem para o log de eventos.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Define as informações sobre um nível de política.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Define os controles de política global.<br/>                                                                                                                                          |



 

 

