---
title: A função midl_user_free
description: A \_ função gratuita do usuário MIDL \_ deve ser fornecida por desenvolvedores de RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366624"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="dd723-103">A \_ função gratuita do usuário MIDL \_</span><span class="sxs-lookup"><span data-stu-id="dd723-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="dd723-104">A **função \_ \_ gratuita do usuário MIDL** deve ser fornecida por desenvolvedores de RPC.</span><span class="sxs-lookup"><span data-stu-id="dd723-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="dd723-105">Ele aloca memória para os stubs RPC e rotinas de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dd723-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="dd723-106">A **função \_ \_ gratuita do usuário MIDL** deve corresponder ao seguinte protótipo:</span><span class="sxs-lookup"><span data-stu-id="dd723-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="dd723-107">O parâmetro *pBuffer* especifica um ponteiro para a memória a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="dd723-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="dd723-108">O aplicativo cliente e o aplicativo de servidor devem implementar a função do **\_ usuário \_ MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="dd723-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="dd723-109">A função de **\_ usuário \_ de MIDL** deve ser capaz de liberar todo o armazenamento alocado por [**\_ \_ alocação de usuário MIDL**](the-midl-user-allocate-function.md).</span><span class="sxs-lookup"><span data-stu-id="dd723-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="dd723-110">Aplicativos e stubs chamam o **\_ usuário MIDL \_ gratuito** ao lidar com objetos alocados:</span><span class="sxs-lookup"><span data-stu-id="dd723-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="dd723-111">O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ gratuitamente** para liberar memória alocada pelo aplicativo, como ao excluir um nó de dados alocado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="dd723-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="dd723-112">O stub de servidor chama o **\_ usuário MIDL \_ gratuitamente** para liberar memória no servidor após o marshaling de todos os \[ \] argumentos, os \[ \] argumentos de \[ saída \] e o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="dd723-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="dd723-113">Por exemplo, o programa de exemplo RPC do Windows que exibe "Olá, mundo" implementa o **\_ usuário MIDL \_ gratuitamente** em termos da função C livre:</span><span class="sxs-lookup"><span data-stu-id="dd723-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="dd723-114">Se o pacote RpcSs estiver habilitado (por exemplo, como resultado do uso do atributo \[ [**habilitar \_ alocação**](/windows/desktop/Midl/enable-allocate) \] ), o programa do servidor deverá usar o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="dd723-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="dd723-115">Para obter mais informações, consulte [pacote de gerenciamento de memória do RPCSS](rpcss-memory-management-package.md).</span><span class="sxs-lookup"><span data-stu-id="dd723-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 