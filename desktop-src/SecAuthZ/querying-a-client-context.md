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
# <a name="querying-a-client-context"></a>Consultando um contexto de cliente

Os aplicativos podem chamar a função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar informações sobre um contexto de cliente existente.

O parâmetro *InfoClass* da função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) usa um valor da enumeração de [**\_ \_ \_ classe de informações do contexto AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) que especifica o tipo de informações que a função consulta.

As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional; caso contrário, o termo de expressão condicional que os referenciará será avaliado como desconhecido. Para obter mais informações sobre expressões condicionais, consulte o tópico [Security Descriptor Definition Language para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Exemplo

O exemplo a seguir consulta o contexto de cliente criado no exemplo da [inicialização de um contexto de cliente](initializing-a-client-context.md) para recuperar a lista de [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) de grupos associados a esse contexto de cliente.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando SIDs a um contexto de cliente](adding-sids-to-a-client-context.md)
</dt> <dt>

[Cache de verificações de acesso](caching-access-checks.md)
</dt> <dt>

[Verificando o acesso com a API AuthZ](checking-access-with-authz-api.md)
</dt> <dt>

[Como a AccessCheck funciona](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Inicializando um contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



