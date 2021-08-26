---
title: Alças de associação primitivas e personalizadas
description: Todos os alças declarados com os tipos \_ handle t ou RPC BINDING HANDLE \_ são \_ alças de associação primitivas.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019146"
---
# <a name="primitive-and-custom-binding-handles"></a>Alças de associação primitivas e personalizadas

Todos os alças declarados com os tipos [ \_ handle t](/windows/desktop/Midl/handle-t) ou [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) são alças de associação primitivas. Você pode estender os tipos [ \_ handle t](/windows/desktop/Midl/handle-t) ou [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) para incluir mais informações ou informações diferentes do que o tipo de identificador primitivo contém. Ao fazer isso, você cria um alça de associação personalizada.

Para criar um identificador de associação personalizado para seu aplicativo distribuído, você precisará criar seu próprio tipo de dados e especificar o atributo handle em uma definição de tipo no arquivo \[ [](/windows/desktop/Midl/handle) \] IDL. Por fim, os arquivos stub mapeiam alças de associação personalizadas para alças primitivas.

Se você criar seu próprio tipo de identificador de associação, também deverá fornecer rotinas de associação e desa associação que o stub do cliente usa para mapear um identificador personalizado para um identificador primitivo. O stub chama suas rotinas de vinculação e desavinculação no início e no final de cada chamada de procedimento remoto. As rotinas de vinculação e desavinculação devem estar em conformidade com os protótipos de função a seguir.



| Protótipo da função                     | Descrição       |
|----------------------------------------|-------------------|
| handle \_ t type \_ bind(*type*)           | Rotina de associação   |
| void type \_ unbind(*type*, *handle \_ t*) | Rotina de desavinculação |



 

O exemplo a seguir mostra como um alça de associação personalizada pode ser definido no arquivo IDL:

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

Se a rotina de vinculação encontrar um erro, ela deverá criar uma exceção usando a [**função RpcRaiseException.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) Em seguida, o stub do cliente limpará e permitirá que a exceção filtre para o bloco de exceção em torno da chamada de procedimento remoto no lado do cliente. Se a rotina de associação simplesmente retornar **NULL**, o código do cliente obtém o erro RPC \_ S INVALID \_ \_ BINDING. Embora isso possa ser aceitável em determinadas situações, outras situações (como ficar sem memória) não respondem bem. A rotina de desavinculação deve ser projetada para que ela não falhe. A rotina de desavinculação não deve criar exceções.

As rotinas de desavinculação e de vinculação definidas pelo programador aparecem no aplicativo cliente. No exemplo a seguir, a rotina de associação chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para converter as informações de associação de cadeia de caracteres em um alça de associação. A rotina de desa associação [**chama RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o alça de associação.

O nome do identificador de associação definido pelo programador, DATA HANDLE TYPE, aparece como \_ parte do nome das \_ funções. Ele também é usado como o tipo de parâmetro nos parâmetros de função.

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

Os alças de associação implícitas e explícitas podem ser alças primitivas ou personalizadas. Ou seja, um handle pode ser:

-   Primitivo e implícito
-   Personalizado e implícito
-   Primitivo e explícito
-   Personalizado e explícito

 

 