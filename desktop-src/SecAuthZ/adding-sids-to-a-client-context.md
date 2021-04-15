---
description: Um aplicativo pode adicionar SIDs (identificadores de segurança) a um contexto de cliente existente chamando a função AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Adicionando SIDs a um contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506086"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="3dedc-103">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3dedc-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="3dedc-104">Um aplicativo pode adicionar SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) a um contexto de cliente existente chamando a função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="3dedc-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="3dedc-105">A função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permite que um aplicativo especifique uma lista de SIDs e uma lista de SIDs de restrição para o contexto de cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="3dedc-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="3dedc-106">O sistema usa a lista de SIDs de restrição quando verifica o acesso do token a um objeto protegível.</span><span class="sxs-lookup"><span data-stu-id="3dedc-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="3dedc-107">Quando um processo ou thread restrito tenta acessar um objeto protegível, o sistema executa duas verificações de acesso: uma usando os SIDs habilitados do token e outra usando a lista de SIDs de restrição.</span><span class="sxs-lookup"><span data-stu-id="3dedc-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="3dedc-108">O acesso será concedido somente se ambas as verificações de acesso permitirem os direitos de acesso solicitados.</span><span class="sxs-lookup"><span data-stu-id="3dedc-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="3dedc-109">As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="3dedc-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="3dedc-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3dedc-110">Example</span></span>

<span data-ttu-id="3dedc-111">O exemplo a seguir adiciona um SID e um SID restrito ao contexto do cliente criado pelo exemplo na [inicialização de um contexto de cliente](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="3dedc-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="3dedc-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dedc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dedc-113">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="3dedc-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="3dedc-114">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="3dedc-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="3dedc-115">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3dedc-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="3dedc-116">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="3dedc-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
