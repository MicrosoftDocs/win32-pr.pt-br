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
# <a name="initializing-a-client-context"></a>Inicializando um contexto de cliente

Um aplicativo deve criar um contexto de cliente antes de poder usar a API AuthZ para executar verificações de acesso ou auditoria.

Um aplicativo deve chamar a função [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar o Gerenciador de recursos. O aplicativo pode então chamar uma de várias funções para criar um contexto de cliente. Além disso, se você estiver executando verificações de acesso ou auditoria remotamente, deverá usar a função [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .

Para criar um contexto de cliente com base em um contexto de cliente existente, chame a função [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .

A função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) cria um novo contexto de cliente usando as informações em um token de logon. A função [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) cria um novo contexto de cliente usando o [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid)especificado.

Se possível, chame a função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) em vez de [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). O **AuthzInitializeContextFromSid** tenta recuperar as informações disponíveis em um token de logon que o cliente realmente fez logon. Um token de logon real fornece mais informações, como o tipo de logon e as propriedades de logon, e reflete o comportamento do pacote de autenticação usado para o logon. O contexto de cliente criado pelo **AuthzInitializeContextFromToken** usa um token de logon, e o contexto de cliente resultante é mais completo e preciso do que um contexto de cliente criado pelo **AuthzInitializeContextFromSid**.

> [!Note]  
> As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional; caso contrário, o termo de expressão condicional que os referenciará será avaliado como desconhecido. Para obter mais informações sobre expressões condicionais, consulte o tópico [Security Descriptor Definition Language para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Exemplo

O exemplo a seguir inicializa o Gerenciador de recursos do AuthZ e chama a função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para criar um contexto de cliente do token de logon associado ao processo atual.


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

[Consultando um contexto de cliente](querying-a-client-context.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



