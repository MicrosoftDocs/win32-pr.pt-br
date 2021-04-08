---
description: Retornos de chamada usados para exibir texturas.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087673"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="c6b79-103"><span id="vspixengine.ipixengine5callbacks"></span>Interface IPixEngine5Callbacks</span><span class="sxs-lookup"><span data-stu-id="c6b79-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="c6b79-104">Retornos de chamada usados para exibir texturas.</span><span class="sxs-lookup"><span data-stu-id="c6b79-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="c6b79-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c6b79-105">Members</span></span>

<span data-ttu-id="c6b79-106">A interface **IPixEngine5Callbacks** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6b79-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6b79-107">**IPixEngine5Callbacks** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6b79-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="c6b79-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6b79-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c6b79-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c6b79-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c6b79-110">A interface **IPixEngine5Callbacks** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c6b79-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c6b79-111">Método</span><span class="sxs-lookup"><span data-stu-id="c6b79-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c6b79-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6b79-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c6b79-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-114">Uma função de retorno de chamada usada para notificar o host quando uma textura foi liberada.</span><span class="sxs-lookup"><span data-stu-id="c6b79-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c6b79-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-116">Uma função de retorno de chamada usada para notificar o host quando um carregamento de histograma tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="c6b79-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c6b79-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-118">Uma função de retorno de chamada usada para notificar o host quando um carregamento de textura for concluído.</span><span class="sxs-lookup"><span data-stu-id="c6b79-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c6b79-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-120">Uma função de retorno de chamada usada para notificar o host quando um carregamento de fatia de textura tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="c6b79-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c6b79-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-122">Uma função de retorno de chamada usada para notificar o host quando um valor de Texel lido tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="c6b79-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c6b79-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-124">Uma função de retorno de chamada usada para notificar o host quando um processamento de textura tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="c6b79-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c6b79-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6b79-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c6b79-126">Uma função de retorno de chamada usada para notificar o host ao salvar uma textura foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c6b79-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c6b79-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b79-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c6b79-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6b79-128">Header</span></span></p></td><td><span data-ttu-id="c6b79-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c6b79-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
