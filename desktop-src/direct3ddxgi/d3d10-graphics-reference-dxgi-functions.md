---
description: Esta seção contém informações sobre as funções fornecidas pelo DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funções DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500256"
---
# <a name="dxgi-functions"></a><span data-ttu-id="f265e-103">Funções DXGI</span><span class="sxs-lookup"><span data-stu-id="f265e-103">DXGI Functions</span></span>

<span data-ttu-id="f265e-104">Esta seção contém informações sobre as funções fornecidas pelo DXGI.</span><span class="sxs-lookup"><span data-stu-id="f265e-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f265e-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f265e-105">In this section</span></span>



| <span data-ttu-id="f265e-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="f265e-106">Topic</span></span>                                                                                   | <span data-ttu-id="f265e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f265e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f265e-108">**CreateDXGIFactory**</span><span class="sxs-lookup"><span data-stu-id="f265e-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="f265e-109">Cria uma fábrica de DXGI 1,0 que você pode usar para gerar outros objetos DXGI.</span><span class="sxs-lookup"><span data-stu-id="f265e-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f265e-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="f265e-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="f265e-111">Cria uma fábrica de DXGI 1,1 que você pode usar para gerar outros objetos DXGI.</span><span class="sxs-lookup"><span data-stu-id="f265e-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f265e-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="f265e-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="f265e-113">Cria uma fábrica de DXGI 1,3 que você pode usar para gerar outros objetos DXGI.</span><span class="sxs-lookup"><span data-stu-id="f265e-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="f265e-114">No Windows 8, qualquer fábrica de DXGI criado enquanto DXGIDebug.dll estava presente no sistema o carregaria e o usaria.</span><span class="sxs-lookup"><span data-stu-id="f265e-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="f265e-115">A partir do Windows 8.1, os aplicativos solicitam explicitamente que DXGIDebug.dll sejam carregados em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f265e-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="f265e-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) e especifique o \_ sinalizador de depuração de criação de fábrica DXGI \_ \_ para solicitar DXGIDebug.dll; a dll será carregada se estiver presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="f265e-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="f265e-117">**DXGIDeclareAdapterRemovalSupport**</span><span class="sxs-lookup"><span data-stu-id="f265e-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="f265e-118">Permite que um processo indique que ele é resiliente a qualquer um de seus dispositivos gráficos sendo removidos.</span><span class="sxs-lookup"><span data-stu-id="f265e-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f265e-119">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="f265e-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="f265e-120">Recupera uma interface de depuração.</span><span class="sxs-lookup"><span data-stu-id="f265e-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="f265e-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="f265e-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="f265e-122">Recupera uma interface que os aplicativos da Windows Store usam para depurar a infraestrutura gráfica do Microsoft DirectX (DXGI).</span><span class="sxs-lookup"><span data-stu-id="f265e-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="f265e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f265e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f265e-124">Referência DXGI</span><span class="sxs-lookup"><span data-stu-id="f265e-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




