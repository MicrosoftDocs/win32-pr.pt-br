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
# <a name="implicit-binding-handles"></a><span data-ttu-id="07c73-103">Identificadores de associação implícita</span><span class="sxs-lookup"><span data-stu-id="07c73-103">Implicit Binding Handles</span></span>

<span data-ttu-id="07c73-104">Os identificadores de associação implícitas permitem que seu aplicativo selecione um servidor específico para executar suas chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="07c73-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="07c73-105">Para obter detalhes, consulte [associação do lado do cliente](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="07c73-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="07c73-106">Eles também permitem que seu programa cliente/servidor use associações autenticadas.</span><span class="sxs-lookup"><span data-stu-id="07c73-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="07c73-107">Ou seja, o cliente pode especificar informações de autenticação em um identificador de associação implícito.</span><span class="sxs-lookup"><span data-stu-id="07c73-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="07c73-108">A biblioteca de tempo de execução RPC usa as informações de autenticação para estabelecer uma sessão RPC autenticada entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="07c73-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="07c73-109">Para saber mais, consulte [Segurança](security.md).</span><span class="sxs-lookup"><span data-stu-id="07c73-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="07c73-110">Os identificadores de associação implícitas não são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="07c73-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="07c73-111">Os aplicativos multi-threaded, portanto, devem evitar o uso de identificadores de associação implícitos.</span><span class="sxs-lookup"><span data-stu-id="07c73-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="07c73-112">Quando seu aplicativo usa associações implícitas, o cliente deve definir as informações de associação para que possa criar a associação.</span><span class="sxs-lookup"><span data-stu-id="07c73-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="07c73-113">Depois que o cliente cria uma associação implícita, ele não precisa passar identificadores de ligação para procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="07c73-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="07c73-114">A Biblioteca RPC lida com o restante da mecânica da sessão de comunicação.</span><span class="sxs-lookup"><span data-stu-id="07c73-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="07c73-115">O cliente armazena as informações de associação para um identificador implícito em uma variável global.</span><span class="sxs-lookup"><span data-stu-id="07c73-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="07c73-116">Quando o compilador MIDL gera o stub do cliente e o arquivo de cabeçalho da especificação de interface no arquivo MIDL, ele também gera código para uma variável de identificador de associação global.</span><span class="sxs-lookup"><span data-stu-id="07c73-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="07c73-117">O programa cliente Inicializa o identificador e não faz referência a ele novamente até destruir a associação.</span><span class="sxs-lookup"><span data-stu-id="07c73-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="07c73-118">Você cria um identificador implícito especificando o atributo de \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) \] no ACF para uma interface da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="07c73-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="07c73-119">O tipo de **manipulador \_ t** , que é usado no exemplo anterior, é um tipo de dados MIDL usado para definir identificadores de associação.</span><span class="sxs-lookup"><span data-stu-id="07c73-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="07c73-120">Depois de criar o identificador implícito, o aplicativo precisa usá-lo como um parâmetro para as funções de biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="07c73-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="07c73-121">Não use o identificador implícito como um parâmetro para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="07c73-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="07c73-122">O exemplo de código a seguir demonstra o uso de identificadores de associação implícitos.</span><span class="sxs-lookup"><span data-stu-id="07c73-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="07c73-123">No exemplo anterior, as funções de biblioteca de tempo de execução RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) exigiam que o identificador de ligação implícita fosse passado em suas listas de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07c73-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="07c73-124">No entanto, o procedimento remoto MyRemoteProcedure não, pois não é uma função de biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="07c73-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 