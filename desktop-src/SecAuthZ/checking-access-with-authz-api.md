---
description: Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Verificando o acesso com a API AuthZ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876c3b5305e33969f63932fdc9e1e4f6767c95a64b11272283420a377b39f795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783092"
---
# <a name="checking-access-with-authz-api"></a>Verificando o acesso com a API AuthZ

Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

A função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) usa as estruturas de [**\_ \_ solicitação de acesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) e [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) como parâmetros. A estrutura de **\_ \_ solicitação de acesso do AUTHZ** especifica um nível de acesso solicitado. A função **AuthzAccessCheck** avalia o acesso solicitado em relação ao **\_ descritor de segurança** especificado para um contexto de cliente especificado. Para obter informações sobre como um descritor de segurança controla o acesso a um objeto, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).

As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.

## <a name="callback-function"></a>Função de retorno da chamada

Se a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) do objeto a ser verificado contiver quaisquer ACEs (entradas de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada, [**AUTHZACCESSCHECK**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) chamará a função [**AUTHZACCESSCHECKCALLBACK**](authzaccesscheckcallback.md) para cada ACE de retorno de chamada contido na DACL. Uma ACE de retorno de chamada é qualquer estrutura de ACE cujo tipo ACE contenha a palavra "callback". A função **AuthzAccessCheckCallback** é uma função definida pelo aplicativo que deve ser registrada quando o Gerenciador de recursos é inicializado chamando a função [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .

Uma função de retorno de chamada permite que um aplicativo defina a lógica de negócios a ser avaliada em tempo de execução. Quando a função [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) for chamada, a ACE de retorno de chamada que causou a chamada será passada para a função de retorno de chamada para avaliação. Se a lógica definida pelo aplicativo for avaliada como **verdadeira**, a ACE de retorno de chamada será incluída na verificação de acesso. Caso contrário, será ignorada.

## <a name="caching-access-results"></a>Caching Resultados de acesso

Os resultados de uma verificação de acesso podem ser armazenados em cache e usados em chamadas futuras para a função [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . para obter mais informações sobre o cache de verificações de acesso, incluindo um exemplo, consulte [Caching verificações de acesso](caching-access-checks.md).

## <a name="example"></a>Exemplo

O exemplo a seguir cria [**um \_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) que permite acesso de **\_ controle de leitura** a administradores internos. Ele usa esse descritor de segurança para verificar o acesso ao cliente especificado pelo contexto do cliente criado no exemplo na [inicialização de um contexto de cliente](initializing-a-client-context.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando SIDs a um contexto de cliente](adding-sids-to-a-client-context.md)
</dt> <dt>

[Caching Verificações de acesso](caching-access-checks.md)
</dt> <dt>

[Inicializando um contexto de cliente](initializing-a-client-context.md)
</dt> <dt>

[Consultando um contexto de cliente](querying-a-client-context.md)
</dt> </dl>

 

 
