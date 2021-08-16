---
description: Quando um aplicativo executa uma verificação de acesso chamando a função AuthzAccessCheck, os resultados dessa verificação de acesso podem ser armazenados em cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Caching Verificações de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783551"
---
# <a name="caching-access-checks"></a>Caching Verificações de acesso

Quando um aplicativo executa uma verificação de acesso chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , os resultados dessa verificação de acesso podem ser armazenados em cache. Quando o parâmetro *pAuthzHandle* da função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) não for **nulo**, a função executará uma verificação de acesso separada, com uma [**\_ máscara de acesso**](access-mask.md) solicitada de **máximo \_ permitido** e armazenará em cache os resultados dessa verificação. Um identificador para os resultados dessa verificação pode ser passado como o parâmetro *AuthzHandle* para a função [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Isso permite a verificação de acesso mais rápida para um determinado cliente e [*descritores de segurança*](/windows/desktop/SecGloss/s-gly).

Somente a parte estática de uma verificação de acesso pode ser armazenada em cache. Quaisquer ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada ou ACEs que contenham o SID **\_ automático principal** devem ser avaliadas para cada verificação de acesso.

As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.

## <a name="example"></a>Exemplo

O exemplo a seguir verifica o acesso em relação a um resultado em cache de uma verificação de acesso anterior. A verificação de acesso anterior foi executada no exemplo em [verificando o acesso com a API AuthZ](checking-access-with-authz-api.md).


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando SIDs a um contexto de cliente](adding-sids-to-a-client-context.md)
</dt> <dt>

[Verificando o acesso com a API AuthZ](checking-access-with-authz-api.md)
</dt> <dt>

[Inicializando um contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consultando um contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
