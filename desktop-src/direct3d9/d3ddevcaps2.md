---
description: Sinalizadores de funcionalidade do driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343201"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="f982a-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="f982a-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="f982a-104">Sinalizadores de funcionalidade do driver D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="f982a-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="f982a-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="f982a-105">\#define</span></span>                                        | <span data-ttu-id="f982a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f982a-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f982a-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="f982a-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="f982a-108">O dispositivo dá suporte ao mosaico adaptável de patches RT</span><span class="sxs-lookup"><span data-stu-id="f982a-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f982a-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="f982a-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="f982a-110">O dispositivo dá suporte ao mosaico adaptável de N patches.</span><span class="sxs-lookup"><span data-stu-id="f982a-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f982a-111">D3DDEVCAPS2 \_ PODE \_ STRETCHRECT \_ DE \_ TEXTURAS</span><span class="sxs-lookup"><span data-stu-id="f982a-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="f982a-112">O dispositivo dá [**suporte ao StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando uma textura como a origem.</span><span class="sxs-lookup"><span data-stu-id="f982a-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="f982a-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="f982a-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="f982a-114">O dispositivo dá suporte a mapas de deslocamento para N patches.</span><span class="sxs-lookup"><span data-stu-id="f982a-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="f982a-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="f982a-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="f982a-116">O dispositivo dá suporte a mapas de deslocamento pré-mpados para N patches.</span><span class="sxs-lookup"><span data-stu-id="f982a-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="f982a-117">Para obter mais informações sobre mapeamento de deslocamento, consulte [Mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="f982a-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="f982a-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="f982a-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="f982a-119">O dispositivo dá suporte a deslocamentos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f982a-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="f982a-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="f982a-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="f982a-121">Vários elementos de vértice poderão compartilhar o mesmo deslocamento em um fluxo se D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET for definido pelo dispositivo e a declaração de vértice não tiver um elemento \_ com D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="f982a-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="f982a-122">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="f982a-122">Constant Information</span></span>



| <span data-ttu-id="f982a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f982a-123">Requirement</span></span>                         | <span data-ttu-id="f982a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f982a-124">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="f982a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f982a-125">Header</span></span>                   | <span data-ttu-id="f982a-126">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="f982a-126">d3d9caps.h</span></span> |
| <span data-ttu-id="f982a-127">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="f982a-127">Minimum operating system</span></span> | <span data-ttu-id="f982a-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f982a-128">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f982a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f982a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f982a-130">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f982a-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
