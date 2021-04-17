---
description: Os aplicativos podem chamar a função AuthzGetInformationFromContext para consultar informações sobre um contexto de cliente existente.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Consultando um contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756165"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="39932-103">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="39932-103">Querying a Client Context</span></span>

<span data-ttu-id="39932-104">Os aplicativos podem chamar a função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar informações sobre um contexto de cliente existente.</span><span class="sxs-lookup"><span data-stu-id="39932-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="39932-105">O parâmetro *InfoClass* da função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) usa um valor da enumeração de [**\_ \_ \_ classe de informações do contexto AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) que especifica o tipo de informações que a função consulta.</span><span class="sxs-lookup"><span data-stu-id="39932-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="39932-106">As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional; caso contrário, o termo de expressão condicional que os referenciará será avaliado como desconhecido.</span><span class="sxs-lookup"><span data-stu-id="39932-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="39932-107">Para obter mais informações sobre expressões condicionais, consulte o tópico [Security Descriptor Definition Language para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="39932-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="39932-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="39932-108">Example</span></span>

<span data-ttu-id="39932-109">O exemplo a seguir consulta o contexto de cliente criado no exemplo da [inicialização de um contexto de cliente](initializing-a-client-context.md) para recuperar a lista de [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) de grupos associados a esse contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="39932-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="39932-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39932-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39932-111">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="39932-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="39932-112">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="39932-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="39932-113">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="39932-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="39932-114">Como a AccessCheck funciona</span><span class="sxs-lookup"><span data-stu-id="39932-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="39932-115">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="39932-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="39932-116">Linguagem de definição do descritor de segurança para ACEs condicionais</span><span class="sxs-lookup"><span data-stu-id="39932-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



