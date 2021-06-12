---
description: Saiba mais sobre uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo na constante D3DVTXPCAPS.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011079"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="9d725-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="9d725-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="9d725-104">Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d725-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="9d725-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="9d725-105">\#define</span></span>                                | <span data-ttu-id="9d725-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d725-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d725-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="9d725-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="9d725-108">O dispositivo pode fazer luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="9d725-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="9d725-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="9d725-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="9d725-110">O dispositivo pode fazer o visualizador local.</span><span class="sxs-lookup"><span data-stu-id="9d725-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="9d725-111">MATERIAIS D3DVTXPCAPSOURCE7 \_</span><span class="sxs-lookup"><span data-stu-id="9d725-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="9d725-112">Quando esse limite é definido, o dispositivo dá suporte aos estados de material de cor: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="9d725-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="9d725-113">D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="9d725-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="9d725-114">O dispositivo não dá suporte à geração de textura no modo de visualizador não local.</span><span class="sxs-lookup"><span data-stu-id="9d725-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="9d725-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="9d725-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="9d725-116">O dispositivo pode fazer luzes posicionais (inclui ponto e ponto).</span><span class="sxs-lookup"><span data-stu-id="9d725-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="9d725-117">D3DVTXPCAPS \_ TEXASGEN</span><span class="sxs-lookup"><span data-stu-id="9d725-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="9d725-118">O dispositivo pode fazer o texgen.</span><span class="sxs-lookup"><span data-stu-id="9d725-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9d725-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="9d725-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="9d725-120">O dispositivo dá suporte a D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="9d725-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="9d725-121">D3DVTXPCAPS \_ TWEENING</span><span class="sxs-lookup"><span data-stu-id="9d725-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="9d725-122">O dispositivo pode fazer interpolação de vértice.</span><span class="sxs-lookup"><span data-stu-id="9d725-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="9d725-123">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="9d725-123">Constant Information</span></span>



| <span data-ttu-id="9d725-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d725-124">Requirement</span></span>                         | <span data-ttu-id="9d725-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9d725-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="9d725-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d725-126">Header</span></span>                   | <span data-ttu-id="9d725-127">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="9d725-127">d3d9caps.h</span></span> |
| <span data-ttu-id="9d725-128">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="9d725-128">Minimum operating system</span></span> | <span data-ttu-id="9d725-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9d725-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9d725-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d725-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d725-131">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="9d725-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



