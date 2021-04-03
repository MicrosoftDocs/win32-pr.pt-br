---
title: A função midl_user_allocate
description: A \_ função de alocação de usuário MIDL \_ é um procedimento que deve ser fornecido por desenvolvedores de aplicativos RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084726"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="83598-103">A função de alocação de \_ usuário MIDL \_</span><span class="sxs-lookup"><span data-stu-id="83598-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="83598-104">A função de **\_ \_ alocação de usuário MIDL** é um procedimento que deve ser fornecido por desenvolvedores de aplicativos RPC.</span><span class="sxs-lookup"><span data-stu-id="83598-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="83598-105">Ele aloca memória para os stubs RPC e rotinas de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="83598-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="83598-106">A função de **\_ \_ alocação de usuário MIDL** deve corresponder ao seguinte protótipo:</span><span class="sxs-lookup"><span data-stu-id="83598-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="83598-107">O parâmetro *cBytes* especifica o número de bytes a serem alocados.</span><span class="sxs-lookup"><span data-stu-id="83598-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="83598-108">Os aplicativos cliente e os aplicativos de servidor devem implementar a função de **\_ \_ alocação de usuário MIDL** , a menos que você esteja compilando no modo uso-Compatibility (/OSF).</span><span class="sxs-lookup"><span data-stu-id="83598-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="83598-109">Os aplicativos e os stubs gerados chamam o **usuário de MIDL \_ \_ alocar** direta ou indiretamente para gerenciar objetos alocados.</span><span class="sxs-lookup"><span data-stu-id="83598-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="83598-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="83598-110">For example:</span></span>

-   <span data-ttu-id="83598-111">Os aplicativos cliente e servidor chamam **o \_ usuário MIDL \_ ALLOCATE** para alocar memória para o aplicativo, como ao criar um novo nó em uma árvore ou em uma lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="83598-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="83598-112">O stub de servidor chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados no espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="83598-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="83598-113">O stub do cliente chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados do servidor que é referenciado por um \[ \] ponteiro out.</span><span class="sxs-lookup"><span data-stu-id="83598-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="83598-114">Observe que para \[ \] \[ ponteiros in, out \] e \[ Unique \] , o stub do cliente chama o **usuário de MIDL \_ \_ ALLOCATE** somente se o \[ valor do ponteiro exclusivo \] era nulo na entrada e muda para um valor não nulo durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="83598-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="83598-115">Se o \[ \] ponteiro exclusivo não for nulo na entrada, o stub do cliente gravará os dados associados em uma memória existente.</span><span class="sxs-lookup"><span data-stu-id="83598-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="83598-116">Se **a \_ \_ alocação de usuário MIDL** falhar ao alocar memória, ela deverá retornar um ponteiro nulo.</span><span class="sxs-lookup"><span data-stu-id="83598-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="83598-117">A função de **\_ \_ alocação de usuário MIDL** deve retornar um ponteiro alinhado de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="83598-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="83598-118">Por exemplo, os programas de exemplo fornecidos com a plataforma SDK (Software Development Kit) implementam a **\_ \_ alocação de usuário de MIDL** em termos da função [**malloc**](pointers-and-memory-allocation.md)C:</span><span class="sxs-lookup"><span data-stu-id="83598-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="83598-119">Se o pacote RpcSs estiver habilitado (por exemplo, como resultado do uso do atributo \[ [**habilitar \_ alocação**](/windows/desktop/Midl/enable-allocate) \] ), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) para alocar memória no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="83598-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="83598-120">Para obter informações adicionais sobre \[ **habilitar \_ alocar** \] , consulte [referência de MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="83598-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 