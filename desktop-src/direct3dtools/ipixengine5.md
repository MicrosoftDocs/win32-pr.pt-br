---
description: Extensões para a interface IPixEngine4 que contém inclusões para exibição de texturas.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500383"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="bf45f-103"><span id="vspixengine.ipixengine5"></span>Interface IPixEngine5</span><span class="sxs-lookup"><span data-stu-id="bf45f-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="bf45f-104">Extensões para a interface IPixEngine4 que contém inclusões para exibição de texturas.</span><span class="sxs-lookup"><span data-stu-id="bf45f-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="bf45f-105">Membros</span><span class="sxs-lookup"><span data-stu-id="bf45f-105">Members</span></span>

<span data-ttu-id="bf45f-106">A interface **IPixEngine5** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bf45f-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bf45f-107">**IPixEngine5** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf45f-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="bf45f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf45f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="bf45f-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="bf45f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="bf45f-110">A interface **IPixEngine5** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="bf45f-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="bf45f-111">Método</span><span class="sxs-lookup"><span data-stu-id="bf45f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="bf45f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf45f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bf45f-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-114">Libera uma textura e notifica o host de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bf45f-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bf45f-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-116">Uma solicitação assíncrona para carregar dados de histograma.</span><span class="sxs-lookup"><span data-stu-id="bf45f-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bf45f-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-118">Carrega uma textura de um arquivo e notifica o host de forma assíncrona quando ele é concluído.</span><span class="sxs-lookup"><span data-stu-id="bf45f-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bf45f-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-120">Carrega uma fatia de textura e notifica o asynchrnously do host quando ele é concluído.</span><span class="sxs-lookup"><span data-stu-id="bf45f-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bf45f-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-122">Lê um valor Texel e retorna o resultado para o host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="bf45f-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bf45f-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-124">Renderiza uma textura em um arquivo e retorna o resultado para o host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="bf45f-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bf45f-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf45f-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bf45f-126">Salva uma textura.</span><span class="sxs-lookup"><span data-stu-id="bf45f-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="bf45f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf45f-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bf45f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf45f-128">Header</span></span></p></td><td><span data-ttu-id="bf45f-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bf45f-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
