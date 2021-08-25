---
description: Um aplicativo deve criar um contexto de cliente antes de poder usar Authz API para executar verificações de acesso ou auditoria.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inicializando um contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908036"
---
# <a name="initializing-a-client-context"></a>Inicializando um contexto de cliente

Um aplicativo deve criar um contexto de cliente antes de poder usar Authz API para executar verificações de acesso ou auditoria.

Um aplicativo deve chamar [**a função AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar o gerenciador de recursos. Em seguida, o aplicativo pode chamar uma das várias funções para criar um contexto de cliente. Além disso, se você estiver executando verificações de acesso ou auditando remotamente, deverá usar a função [**AuthzInitializeRemoteResourceManager.**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)

Para criar um contexto de cliente com base em um contexto de cliente existente, chame a [**função AuthzInitializeContextFromAuthzContext.**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)

A [**função AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) cria um novo contexto de cliente usando informações em um token de logon. A [**função AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) cria um novo contexto de cliente usando o [**SID especificado.**](/windows/desktop/api/Winnt/ns-winnt-sid)

Se possível, chame [**a função AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) em vez de [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** tenta recuperar as informações disponíveis em um token de logon se o cliente realmente fez logon. Um token de logon real fornece mais informações, como o tipo de logon e as propriedades de logon, e reflete o comportamento do pacote de autenticação usado para o logon. O contexto do cliente criado por **AuthzInitializeContextFromToken** usa um token de logon e o contexto do cliente resultante é mais completo e preciso do que um contexto de cliente criado por **AuthzInitializeContextFromSid**.

> [!Note]  
> As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional; caso contrário, o termo de expressão condicional que os referencia será avaliado como desconhecido. Para obter mais informações sobre expressões condicionais, consulte o tópico Linguagem de Definição do Descritor de Segurança [para ACEs](security-descriptor-definition-language-for-conditional-aces-.md) condicionais.

 

## <a name="example"></a>Exemplo

O exemplo a seguir inicializa o gerenciador de recursos Authz e chama a função [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para criar um contexto de cliente do token de logon associado ao processo atual.


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

[Caching Verificações de acesso](caching-access-checks.md)
</dt> <dt>

[Verificando o acesso com Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Como o AccessCheck funciona](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Consultando um contexto de cliente](querying-a-client-context.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



