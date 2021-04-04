---
title: Identificadores de associação implícita
description: Os identificadores de associação implícitas permitem que seu aplicativo selecione um servidor específico para executar suas chamadas de procedimento remoto.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007658"
---
# <a name="implicit-binding-handles"></a>Identificadores de associação implícita

Os identificadores de associação implícitas permitem que seu aplicativo selecione um servidor específico para executar suas chamadas de procedimento remoto. Para obter detalhes, consulte [associação do lado do cliente](client-side-binding.md). Eles também permitem que seu programa cliente/servidor use associações autenticadas. Ou seja, o cliente pode especificar informações de autenticação em um identificador de associação implícito. A biblioteca de tempo de execução RPC usa as informações de autenticação para estabelecer uma sessão RPC autenticada entre o cliente e o servidor. Para saber mais, consulte [Segurança](security.md).

> [!Note]  
> Os identificadores de associação implícitas não são thread-safe. Os aplicativos multi-threaded, portanto, devem evitar o uso de identificadores de associação implícitos.

 

Quando seu aplicativo usa associações implícitas, o cliente deve definir as informações de associação para que possa criar a associação. Depois que o cliente cria uma associação implícita, ele não precisa passar identificadores de ligação para procedimentos remotos. A Biblioteca RPC lida com o restante da mecânica da sessão de comunicação.

O cliente armazena as informações de associação para um identificador implícito em uma variável global. Quando o compilador MIDL gera o stub do cliente e o arquivo de cabeçalho da especificação de interface no arquivo MIDL, ele também gera código para uma variável de identificador de associação global. O programa cliente Inicializa o identificador e não faz referência a ele novamente até destruir a associação.

Você cria um identificador implícito especificando o atributo de \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] no ACF para uma interface da seguinte maneira:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

O tipo de **manipulador \_ t** , que é usado no exemplo anterior, é um tipo de dados MIDL usado para definir identificadores de associação.

Depois de criar o identificador implícito, o aplicativo precisa usá-lo como um parâmetro para as funções de biblioteca de tempo de execução RPC. Não use o identificador implícito como um parâmetro para chamadas de procedimento remoto. O exemplo de código a seguir demonstra o uso de identificadores de associação implícitos.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

No exemplo anterior, as funções de biblioteca de tempo de execução RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) exigiam que o identificador de ligação implícita fosse passado em suas listas de parâmetros. No entanto, o procedimento remoto MyRemoteProcedure não, pois não é uma função de biblioteca de tempo de execução RPC.

 

 