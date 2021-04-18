---
description: Modo exclusivo do DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760709"
---
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="bd0be-103">Modo exclusivo do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="bd0be-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="bd0be-104">Este tópico aplica-se somente ao VMR-7.</span><span class="sxs-lookup"><span data-stu-id="bd0be-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="bd0be-105">No VMR-9, você habilita o modo exclusivo fornecendo seu próprio apresentador de alocador de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bd0be-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="bd0be-106">Isso é relativamente simples se você usar o método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) .</span><span class="sxs-lookup"><span data-stu-id="bd0be-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="bd0be-107">O exemplo de VMR9Allocator mostra como implementar um apresentador de alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="bd0be-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="bd0be-108">No modo exclusivo do DirectDraw, um aplicativo assume o controle exclusivo do hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="bd0be-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="bd0be-109">Isso é útil para aplicativos como jogos, ou talvez aplicativos de vídeo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="bd0be-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="bd0be-110">Normalmente, o VMR cria os objetos do DirectDraw e define o nível de cooperação como normal.</span><span class="sxs-lookup"><span data-stu-id="bd0be-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="bd0be-111">No entanto, para executar o VMR no modo exclusivo do DirectDraw, o próprio aplicativo deve criar o objeto do DirectDraw e a superfície primária e chamar **SetCooperativeLevel** para especificar o modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bd0be-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="bd0be-112">O VMR tem um apresentador de alocador especial que permite que ele seja executado no modo exclusivo do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="bd0be-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="bd0be-113">Para configurar o VMR para usar este alocador-Presenter:</span><span class="sxs-lookup"><span data-stu-id="bd0be-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="bd0be-114">Crie o gráfico de filtro e adicione o VMR a ele usando o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) .</span><span class="sxs-lookup"><span data-stu-id="bd0be-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="bd0be-115">Para obter um exemplo de código, consulte [modo sem janela do VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="bd0be-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="bd0be-116">Criar o alocador de modo exclusivo-apresentador:</span><span class="sxs-lookup"><span data-stu-id="bd0be-116">Create the Exclusive Mode allocator-presenter:</span></span>
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  <span data-ttu-id="bd0be-117">Configure o novo alocador-apresentador:</span><span class="sxs-lookup"><span data-stu-id="bd0be-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="bd0be-118">Conecte o novo alocador-apresentador ao VMR.</span><span class="sxs-lookup"><span data-stu-id="bd0be-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="bd0be-119">Compile o restante do grafo de filtro de maneira usual.</span><span class="sxs-lookup"><span data-stu-id="bd0be-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd0be-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd0be-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd0be-121">Modos de operação do VMR</span><span class="sxs-lookup"><span data-stu-id="bd0be-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



