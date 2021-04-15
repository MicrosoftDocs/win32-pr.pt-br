---
title: Pacote de gerenciamento de memória de RpcSs
description: O par de alocador/desalocador padrão usado pelos stubs e o tempo de execução ao alocar memória em nome do aplicativo é o usuário de MIDL \_ \_ alocar/MIDL \_ user \_ Free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454260"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="2f7cd-103">Pacote de gerenciamento de memória de RpcSs</span><span class="sxs-lookup"><span data-stu-id="2f7cd-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="2f7cd-104">O par de alocador/desalocador padrão usado pelos stubs e tempo de execução ao alocar memória em nome do aplicativo é **MIDL \_ usuário \_ alocar** / **usuário de MIDL \_ \_ gratuito**.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="2f7cd-105">No entanto, você pode escolher o pacote RpcSs em vez do padrão usando o atributo ACF **\[ habilitar \_ alocação \]**.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="2f7cd-106">O pacote RpcSs consiste em funções RPC que começam com o prefixo **RPCSS** ou **RPCSS**.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="2f7cd-107">O pacote RpcSs não é recomendado para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="2f7cd-108">O pacote de gerenciamento de memória do RPCSS está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="2f7cd-109">É recomendável que [**o \_ usuário \_ de MIDL aloque**](/windows/desktop/Midl/midl-user-allocate-1) e o [**usuário de MIDL \_ \_ livre**](/windows/desktop/Midl/midl-user-free-1) sejam usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="2f7cd-110">No modo **/OSF** , o pacote RPCSS é habilitado para stubs gerados por MIDL automaticamente quando são usados ponteiros completos, quando os argumentos exigem alocação de memória ou como resultado do uso do atributo **\[ Enable \_ ALLOCATE \]** .</span><span class="sxs-lookup"><span data-stu-id="2f7cd-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="2f7cd-111">No modo padrão (Microsoft Extended), o pacote RpcSs é habilitado somente quando o atributo **\[ habilitar \_ alocação \]** é usado.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="2f7cd-112">O atributo **\[ habilitar \_ alocação \]** habilita o ambiente RPCSS pelos stubs do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="2f7cd-113">O lado do cliente se torna alertado sobre a possibilidade de habilitar o pacote RpcSs.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="2f7cd-114">No modo **/OSF** , o lado do cliente não é afetado.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="2f7cd-115">Quando o pacote RpcSs está habilitado, a alocação de memória no lado do servidor é realizada com o par do alocador de gerenciamento de memória e desalocação de RpcS particulares.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="2f7cd-116">Você pode alocar memória usando o mesmo mecanismo chamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (ou [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span><span class="sxs-lookup"><span data-stu-id="2f7cd-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="2f7cd-117">Após o retorno do stub do servidor, toda a memória alocada pelo pacote RpcSs é liberada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="2f7cd-118">O exemplo a seguir mostra como habilitar o pacote RpcSs:</span><span class="sxs-lookup"><span data-stu-id="2f7cd-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="2f7cd-119">O aplicativo pode liberar memória explicitamente invocando a função [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) ou [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) .</span><span class="sxs-lookup"><span data-stu-id="2f7cd-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="2f7cd-120">Observe que essas funções não liberam realmente a memória.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="2f7cd-121">Eles o marcam para exclusão.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-121">They mark it for deletion.</span></span> <span data-ttu-id="2f7cd-122">A Biblioteca RPC libera a memória quando o programa chama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) ou [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span><span class="sxs-lookup"><span data-stu-id="2f7cd-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="2f7cd-123">Você também pode habilitar o ambiente de gerenciamento de memória para seu aplicativo chamando a rotina [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (e você pode desabilitá-lo chamando a rotina [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ).</span><span class="sxs-lookup"><span data-stu-id="2f7cd-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="2f7cd-124">Uma vez habilitado, o código do aplicativo pode alocar e desalocar memória chamando funções do pacote RpcSs.</span><span class="sxs-lookup"><span data-stu-id="2f7cd-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 