---
title: Identificadores de associação primitivos e personalizados
description: Todos os identificadores declarados com os \_ tipos de identificador de associação t ou RPC \_ \_ são identificadores de associação primitivos.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008049"
---
# <a name="primitive-and-custom-binding-handles"></a>Identificadores de associação primitivos e personalizados

Todos os identificadores declarados com os tipos de [**\_ \_ identificador de associação**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) ou RPC são identificadores de associação primitivos. Você pode estender os tipos de [**identificador de \_ Associação \_**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) ou RPC para incluir mais ou informações diferentes do que o tipo de identificador primitivo contém. Ao fazer isso, você cria um identificador de ligação personalizado.

Para fazer um identificador de ligação personalizado para seu aplicativo distribuído, você precisará criar seu próprio tipo de dados e especificar o \[ [](/windows/desktop/Midl/handle) \] atributo Handle em uma definição de tipo em seu arquivo IDL. Por fim, os arquivos stub mapeiam identificadores de associação personalizados para identificadores primitivos.

Se você criar seu próprio tipo de identificador de associação, também deverá fornecer rotinas de ligação e desvinculação que o stub de cliente usa para mapear um identificador personalizado para um identificador primitivo. O stub chama suas rotinas BIND e Unbind no início e no final de cada chamada de procedimento remoto. As rotinas de associação e desvinculação devem estar de acordo com os seguintes protótipos de função.



| Protótipo da função                     | Description       |
|----------------------------------------|-------------------|
| tratar \_ \_ Associação de tipo t (*tipo*)           | Rotina de associação   |
| tipo void \_ desassociar (*tipo*, *identificador \_ t*) | Desassociando rotina |



 

O exemplo a seguir mostra como um identificador de ligação personalizado pode ser definido no arquivo IDL:

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Se a rotina de associação encontrar um erro, ela deverá gerar uma exceção usando a função [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) . O stub do cliente será limpo e permitirá que a exceção seja filtrada para o bloco de exceção em torno da chamada de procedimento remoto no lado do cliente. Se a rotina de associação simplesmente retornar **NULL**, o código do cliente receberá uma associação de RPC \_ S \_ inválida \_ . Embora isso possa ser aceitável em determinadas situações, outras situações (como memória insuficiente) não respondem bem. A rotina de desassociar deve ser projetada para que não falhe. A rotina de desassociar não deve gerar exceções.

As rotinas de associação e desvinculação definidas pelo programador aparecem no aplicativo cliente. No exemplo a seguir, a rotina BIND chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para converter as informações de associação de cadeia de caracteres em um identificador de associação. A rotina desassociar chama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o identificador de associação.

O nome do identificador de associação definido pelo programador, o \_ tipo de identificador de dados \_ , aparece como parte do nome das funções. Ele também é usado como o tipo de parâmetro nos parâmetros de função.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Os identificadores de ligação implícitos e explícitos podem ser identificadores primitivos ou personalizados. Ou seja, um identificador pode ser:

-   Primitivo e implícito
-   Personalizado e implícito
-   Primitivo e explícito
-   Personalizado e explícito

 

 