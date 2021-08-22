---
title: Alças de associação implícitas
description: Os alças de associação implícita permitem que seu aplicativo selecione um servidor específico para executar suas chamadas de procedimento remoto.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d49618ec505cc776c346a504fb19b65db539dadb90d030e45efbabcf08371db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929071"
---
# <a name="implicit-binding-handles"></a>Alças de associação implícitas

Os alças de associação implícita permitem que seu aplicativo selecione um servidor específico para executar suas chamadas de procedimento remoto. Para obter detalhes, consulte [Associação do lado do cliente.](client-side-binding.md) Eles também permitem que seu programa cliente/servidor use vinculações autenticadas. Ou seja, o cliente pode especificar informações de autenticação em um alçamento de associação implícito. A biblioteca em tempo de executar RPC usa as informações de autenticação para estabelecer uma sessão RPC autenticada entre o cliente e o servidor. Para saber mais, consulte [Segurança](security.md).

> [!Note]  
> Os alças de associação implícita não são thread-safe. Portanto, os aplicativos multi-threaded devem evitar o uso de alças de associação implícita.

 

Quando seu aplicativo usa vinculações implícitas, o cliente deve definir as informações de associação para que ele possa criar a associação. Depois que o cliente cria uma associação implícita, ele não precisa passar nenhum tipo de alça de associação para procedimentos remotos. A biblioteca RPC lida com o restante da mecânica da sessão de comunicação.

O cliente armazena as informações de associação para um alça implícito em uma variável global. Quando o compilador MIDL gera o stub do cliente e o arquivo de header da especificação de interface em seu arquivo MIDL, ele também gera código para uma variável de alça de associação global. O programa cliente inicializa o handle e, em seguida, não se refere a ele novamente até destruir a associação.

Você cria um alça implícito especificando o atributo \[ [**\_ de alça**](/windows/desktop/Midl/implicit-handle) implícita no \] ACF para uma interface da seguinte forma:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

O **tipo \_ t** do identificador, que é usado no exemplo anterior, é um tipo de dados MIDL usado para definir identificador de associação.

Depois de criar o alça implícito, o aplicativo precisa usá-lo como um parâmetro para as funções de biblioteca em tempo de executar RPC. Não use o alça implícito como um parâmetro para chamadas de procedimento remoto. O exemplo de código a seguir demonstra o uso de alças de associação implícita.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

No exemplo anterior, as funções de biblioteca em tempo de executar [**RPC RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) exigiam que o controle de associação implícito fosse passado em suas listas de parâmetros. No entanto, o procedimento remoto MyRemoteProcedure não fez isso, pois não é uma função de biblioteca em tempo de executar RPC.

 

 