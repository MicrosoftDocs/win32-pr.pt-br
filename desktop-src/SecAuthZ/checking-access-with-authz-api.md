---
description: Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Verificando o acesso com a API AuthZ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827255"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="60514-103">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="60514-103">Checking Access with Authz API</span></span>

<span data-ttu-id="60514-104">Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="60514-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="60514-105">A função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) usa as estruturas de [**\_ \_ solicitação de acesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) e [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="60514-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="60514-106">A estrutura de **\_ \_ solicitação de acesso do AUTHZ** especifica um nível de acesso solicitado.</span><span class="sxs-lookup"><span data-stu-id="60514-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="60514-107">A função **AuthzAccessCheck** avalia o acesso solicitado em relação ao **\_ descritor de segurança** especificado para um contexto de cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="60514-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="60514-108">Para obter informações sobre como um descritor de segurança controla o acesso a um objeto, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="60514-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="60514-109">As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="60514-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="60514-110">Função de retorno da chamada</span><span class="sxs-lookup"><span data-stu-id="60514-110">Callback Function</span></span>

<span data-ttu-id="60514-111">Se a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) do objeto a ser verificado contiver quaisquer ACEs (entradas de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada, [**AUTHZACCESSCHECK**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) chamará a função [**AUTHZACCESSCHECKCALLBACK**](authzaccesscheckcallback.md) para cada ACE de retorno de chamada contido na DACL.</span><span class="sxs-lookup"><span data-stu-id="60514-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="60514-112">Uma ACE de retorno de chamada é qualquer estrutura de ACE cujo tipo ACE contenha a palavra "callback".</span><span class="sxs-lookup"><span data-stu-id="60514-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="60514-113">A função **AuthzAccessCheckCallback** é uma função definida pelo aplicativo que deve ser registrada quando o Gerenciador de recursos é inicializado chamando a função [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="60514-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="60514-114">Uma função de retorno de chamada permite que um aplicativo defina a lógica de negócios a ser avaliada em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="60514-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="60514-115">Quando a função [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) for chamada, a ACE de retorno de chamada que causou a chamada será passada para a função de retorno de chamada para avaliação.</span><span class="sxs-lookup"><span data-stu-id="60514-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="60514-116">Se a lógica definida pelo aplicativo for avaliada como **verdadeira**, a ACE de retorno de chamada será incluída na verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="60514-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="60514-117">Caso contrário, será ignorada.</span><span class="sxs-lookup"><span data-stu-id="60514-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="60514-118">Cache de resultados de acesso</span><span class="sxs-lookup"><span data-stu-id="60514-118">Caching Access Results</span></span>

<span data-ttu-id="60514-119">Os resultados de uma verificação de acesso podem ser armazenados em cache e usados em chamadas futuras para a função [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="60514-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="60514-120">Para obter mais informações sobre o cache de verificações de acesso, incluindo um exemplo, consulte [Caching Access checks](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="60514-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="60514-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="60514-121">Example</span></span>

<span data-ttu-id="60514-122">O exemplo a seguir cria [**um \_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) que permite acesso de **\_ controle de leitura** a administradores internos.</span><span class="sxs-lookup"><span data-stu-id="60514-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="60514-123">Ele usa esse descritor de segurança para verificar o acesso ao cliente especificado pelo contexto do cliente criado no exemplo na [inicialização de um contexto de cliente](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="60514-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="60514-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60514-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60514-125">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="60514-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="60514-126">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="60514-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="60514-127">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="60514-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="60514-128">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="60514-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
