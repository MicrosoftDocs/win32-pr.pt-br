---
description: Sinalizadores de capacidade do driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999463"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="ef25e-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="ef25e-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="ef25e-104">Sinalizadores de capacidade do driver D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="ef25e-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="ef25e-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="ef25e-105">\#define</span></span>                                        | <span data-ttu-id="ef25e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef25e-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef25e-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="ef25e-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="ef25e-108">O dispositivo dá suporte a mosaico adaptável de RT-patches</span><span class="sxs-lookup"><span data-stu-id="ef25e-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="ef25e-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="ef25e-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="ef25e-110">O dispositivo dá suporte a mosaico adaptável de N-patches.</span><span class="sxs-lookup"><span data-stu-id="ef25e-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="ef25e-111">D3DDEVCAPS2 \_ pode \_ STRETCHRECT \_ de \_ texturas</span><span class="sxs-lookup"><span data-stu-id="ef25e-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="ef25e-112">O dispositivo dá suporte a [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando uma textura como a origem.</span><span class="sxs-lookup"><span data-stu-id="ef25e-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="ef25e-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="ef25e-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="ef25e-114">O dispositivo dá suporte a mapas de substituição para N-patches.</span><span class="sxs-lookup"><span data-stu-id="ef25e-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ef25e-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="ef25e-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="ef25e-116">O dispositivo dá suporte a mapas de deslocamento de amostra para N-patches.</span><span class="sxs-lookup"><span data-stu-id="ef25e-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="ef25e-117">Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="ef25e-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="ef25e-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="ef25e-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="ef25e-119">O dispositivo dá suporte a deslocamentos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ef25e-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="ef25e-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="ef25e-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="ef25e-121">Vários elementos de vértice podem compartilhar o mesmo deslocamento em um fluxo se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET for definido pelo dispositivo e a declaração de vértice não tiver um elemento com D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="ef25e-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="ef25e-122">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="ef25e-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="ef25e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef25e-123">Header</span></span>                   | <span data-ttu-id="ef25e-124">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="ef25e-124">d3d9caps.h</span></span> |
| <span data-ttu-id="ef25e-125">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="ef25e-125">Minimum operating system</span></span> | <span data-ttu-id="ef25e-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ef25e-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ef25e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef25e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef25e-128">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="ef25e-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
