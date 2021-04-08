---
description: Sinalizadores de capacidade da coordenada de textura do driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920544"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="79b7d-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="79b7d-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="79b7d-104">Sinalizadores de capacidade da coordenada de textura do driver.</span><span class="sxs-lookup"><span data-stu-id="79b7d-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b7d-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="79b7d-105">\#define</span></span>                                 | <span data-ttu-id="79b7d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="79b7d-106">Value</span></span>       | <span data-ttu-id="79b7d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="79b7d-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="79b7d-108">D3DTSS \_ TCI \_ PassThru</span><span class="sxs-lookup"><span data-stu-id="79b7d-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="79b7d-109">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="79b7d-109">0x00000000L</span></span> | <span data-ttu-id="79b7d-110">Use as coordenadas de textura especificadas contidas no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="79b7d-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="79b7d-111">Esse valor é resolvido para zero.</span><span class="sxs-lookup"><span data-stu-id="79b7d-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="79b7d-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="79b7d-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="79b7d-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="79b7d-113">0x00010000L</span></span> | <span data-ttu-id="79b7d-114">Use o vértice normal, transformado no espaço da câmera, como as coordenadas de textura de entrada para a transformação textura desta etapa.</span><span class="sxs-lookup"><span data-stu-id="79b7d-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="79b7d-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="79b7d-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="79b7d-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="79b7d-116">0x00020000L</span></span> | <span data-ttu-id="79b7d-117">Use a posição do vértice, transformada no espaço da câmera, como as coordenadas de textura de entrada para a transformação textura desta etapa.</span><span class="sxs-lookup"><span data-stu-id="79b7d-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="79b7d-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="79b7d-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="79b7d-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="79b7d-119">0x00030000L</span></span> | <span data-ttu-id="79b7d-120">Use o vetor de reflexo, transformado no espaço da câmera, como a coordenada de textura de entrada para a transformação textura desta etapa.</span><span class="sxs-lookup"><span data-stu-id="79b7d-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="79b7d-121">O vetor de reflexão é calculado a partir da posição do vértice de entrada e do vetor normal.</span><span class="sxs-lookup"><span data-stu-id="79b7d-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="79b7d-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="79b7d-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="79b7d-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="79b7d-123">0x00040000L</span></span> | <span data-ttu-id="79b7d-124">Use as coordenadas de textura especificadas para o mapeamento de esfera.</span><span class="sxs-lookup"><span data-stu-id="79b7d-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="79b7d-125">Essas constantes são usadas por D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="79b7d-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="79b7d-126">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="79b7d-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="79b7d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79b7d-127">Header</span></span>                   | <span data-ttu-id="79b7d-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="79b7d-128">d3d9caps.h</span></span> |
| <span data-ttu-id="79b7d-129">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="79b7d-129">Minimum operating system</span></span> | <span data-ttu-id="79b7d-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="79b7d-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="79b7d-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79b7d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79b7d-132">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="79b7d-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



