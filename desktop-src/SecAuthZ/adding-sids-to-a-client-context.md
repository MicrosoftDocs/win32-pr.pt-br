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
# <a name="adding-sids-to-a-client-context"></a>Adicionando SIDs a um contexto de cliente

Um aplicativo pode adicionar SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) a um contexto de cliente existente chamando a função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) . A função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permite que um aplicativo especifique uma lista de SIDs e uma lista de SIDs de restrição para o contexto de cliente especificado.

O sistema usa a lista de SIDs de restrição quando verifica o acesso do token a um objeto protegível. Quando um processo ou thread restrito tenta acessar um objeto protegível, o sistema executa duas verificações de acesso: uma usando os SIDs habilitados do token e outra usando a lista de SIDs de restrição. O acesso será concedido somente se ambas as verificações de acesso permitirem os direitos de acesso solicitados.

As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.

## <a name="example"></a>Exemplo

O exemplo a seguir adiciona um SID e um SID restrito ao contexto do cliente criado pelo exemplo na [inicialização de um contexto de cliente](initializing-a-client-context.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cache de verificações de acesso](caching-access-checks.md)
</dt> <dt>

[Verificando o acesso com a API AuthZ](checking-access-with-authz-api.md)
</dt> <dt>

[Inicializando um contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consultando um contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
