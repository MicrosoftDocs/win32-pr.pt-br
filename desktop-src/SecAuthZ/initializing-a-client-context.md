---
description: Um aplicativo deve criar um contexto de cliente antes de poder usar a API AuthZ para executar verificações de acesso ou auditoria.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inicializando um contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756570"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="1c385-103">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="1c385-103">Initializing a Client Context</span></span>

<span data-ttu-id="1c385-104">Um aplicativo deve criar um contexto de cliente antes de poder usar a API AuthZ para executar verificações de acesso ou auditoria.</span><span class="sxs-lookup"><span data-stu-id="1c385-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="1c385-105">Um aplicativo deve chamar a função [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar o Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c385-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="1c385-106">O aplicativo pode então chamar uma de várias funções para criar um contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="1c385-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="1c385-107">Além disso, se você estiver executando verificações de acesso ou auditoria remotamente, deverá usar a função [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="1c385-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="1c385-108">Para criar um contexto de cliente com base em um contexto de cliente existente, chame a função [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .</span><span class="sxs-lookup"><span data-stu-id="1c385-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="1c385-109">A função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) cria um novo contexto de cliente usando as informações em um token de logon.</span><span class="sxs-lookup"><span data-stu-id="1c385-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="1c385-110">A função [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) cria um novo contexto de cliente usando o [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid)especificado.</span><span class="sxs-lookup"><span data-stu-id="1c385-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="1c385-111">Se possível, chame a função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) em vez de [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span><span class="sxs-lookup"><span data-stu-id="1c385-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="1c385-112">O **AuthzInitializeContextFromSid** tenta recuperar as informações disponíveis em um token de logon que o cliente realmente fez logon.</span><span class="sxs-lookup"><span data-stu-id="1c385-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="1c385-113">Um token de logon real fornece mais informações, como o tipo de logon e as propriedades de logon, e reflete o comportamento do pacote de autenticação usado para o logon.</span><span class="sxs-lookup"><span data-stu-id="1c385-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="1c385-114">O contexto de cliente criado pelo **AuthzInitializeContextFromToken** usa um token de logon, e o contexto de cliente resultante é mais completo e preciso do que um contexto de cliente criado pelo **AuthzInitializeContextFromSid**.</span><span class="sxs-lookup"><span data-stu-id="1c385-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="1c385-115">As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional; caso contrário, o termo de expressão condicional que os referenciará será avaliado como desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1c385-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="1c385-116">Para obter mais informações sobre expressões condicionais, consulte o tópico [Security Descriptor Definition Language para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="1c385-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="1c385-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1c385-117">Example</span></span>

<span data-ttu-id="1c385-118">O exemplo a seguir inicializa o Gerenciador de recursos do AuthZ e chama a função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para criar um contexto de cliente do token de logon associado ao processo atual.</span><span class="sxs-lookup"><span data-stu-id="1c385-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="1c385-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c385-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c385-120">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="1c385-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="1c385-121">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="1c385-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="1c385-122">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="1c385-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="1c385-123">Como a AccessCheck funciona</span><span class="sxs-lookup"><span data-stu-id="1c385-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="1c385-124">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="1c385-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="1c385-125">Linguagem de definição do descritor de segurança para ACEs condicionais</span><span class="sxs-lookup"><span data-stu-id="1c385-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="1c385-126">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="1c385-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="1c385-127">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="1c385-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



