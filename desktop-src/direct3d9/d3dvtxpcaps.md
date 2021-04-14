---
description: Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370494"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="24b9d-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="24b9d-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="24b9d-104">Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24b9d-104">A combination of one or more flags that control the device create behavior.</span></span>



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b9d-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="24b9d-105">\#define</span></span>                                | <span data-ttu-id="24b9d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="24b9d-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="24b9d-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="24b9d-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="24b9d-108">O dispositivo pode realizar luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="24b9d-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="24b9d-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="24b9d-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="24b9d-110">O dispositivo pode fazer o visualizador local.</span><span class="sxs-lookup"><span data-stu-id="24b9d-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="24b9d-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="24b9d-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="24b9d-112">Quando esse limite é definido, o dispositivo dá suporte aos Estados de material de cor: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DiffuseMaterialSource, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="24b9d-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="24b9d-113">D3DVTXPCAPS \_ \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="24b9d-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="24b9d-114">O dispositivo não oferece suporte à geração de textura no modo de visualizador não local.</span><span class="sxs-lookup"><span data-stu-id="24b9d-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="24b9d-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="24b9d-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="24b9d-116">O dispositivo pode fazer luzes posicionais (inclui ponto e spot).</span><span class="sxs-lookup"><span data-stu-id="24b9d-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="24b9d-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="24b9d-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="24b9d-118">O dispositivo pode fazer texgen.</span><span class="sxs-lookup"><span data-stu-id="24b9d-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="24b9d-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="24b9d-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="24b9d-120">O dispositivo dá suporte a D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="24b9d-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="24b9d-121">\_Interpolação D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="24b9d-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="24b9d-122">O dispositivo pode fazer a interpolação de vértice.</span><span class="sxs-lookup"><span data-stu-id="24b9d-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="24b9d-123">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="24b9d-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="24b9d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b9d-124">Header</span></span>                   | <span data-ttu-id="24b9d-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="24b9d-125">d3d9caps.h</span></span> |
| <span data-ttu-id="24b9d-126">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="24b9d-126">Minimum operating system</span></span> | <span data-ttu-id="24b9d-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="24b9d-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="24b9d-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24b9d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24b9d-129">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="24b9d-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



