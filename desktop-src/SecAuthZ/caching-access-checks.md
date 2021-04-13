---
description: Quando um aplicativo executa uma verificação de acesso chamando a função AuthzAccessCheck, os resultados dessa verificação de acesso podem ser armazenados em cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Cache de verificações de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297766"
---
# <a name="caching-access-checks"></a><span data-ttu-id="3d309-103">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="3d309-103">Caching Access Checks</span></span>

<span data-ttu-id="3d309-104">Quando um aplicativo executa uma verificação de acesso chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , os resultados dessa verificação de acesso podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="3d309-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="3d309-105">Quando o parâmetro *pAuthzHandle* da função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) não for **nulo**, a função executará uma verificação de acesso separada, com uma [**\_ máscara de acesso**](access-mask.md) solicitada de **máximo \_ permitido** e armazenará em cache os resultados dessa verificação.</span><span class="sxs-lookup"><span data-stu-id="3d309-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="3d309-106">Um identificador para os resultados dessa verificação pode ser passado como o parâmetro *AuthzHandle* para a função [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="3d309-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="3d309-107">Isso permite a verificação de acesso mais rápida para um determinado cliente e [*descritores de segurança*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="3d309-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="3d309-108">Somente a parte estática de uma verificação de acesso pode ser armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="3d309-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="3d309-109">Quaisquer ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada ou ACEs que contenham o SID **\_ automático principal** devem ser avaliadas para cada verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="3d309-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="3d309-110">As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="3d309-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="3d309-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3d309-111">Example</span></span>

<span data-ttu-id="3d309-112">O exemplo a seguir verifica o acesso em relação a um resultado em cache de uma verificação de acesso anterior.</span><span class="sxs-lookup"><span data-stu-id="3d309-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="3d309-113">A verificação de acesso anterior foi executada no exemplo em [verificando o acesso com a API AuthZ](checking-access-with-authz-api.md).</span><span class="sxs-lookup"><span data-stu-id="3d309-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3d309-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d309-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d309-115">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3d309-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="3d309-116">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="3d309-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="3d309-117">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3d309-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="3d309-118">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3d309-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
