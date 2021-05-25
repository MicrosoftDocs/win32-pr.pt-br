---
description: Constantes de geração de mapas normais.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342851"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="307af-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="307af-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="307af-104">Constantes de geração de mapas normais.</span><span class="sxs-lookup"><span data-stu-id="307af-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="307af-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="307af-105">\#define</span></span>                            | <span data-ttu-id="307af-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="307af-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307af-107">D3DX \_ NORMALMAP \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="307af-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="307af-108">Indica que os pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.</span><span class="sxs-lookup"><span data-stu-id="307af-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="307af-109">D3DX \_ NORMALMAP \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="307af-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="307af-110">Indica que os pixels fora da borda da textura no eixo v devem ser espelhados, não empacotados.</span><span class="sxs-lookup"><span data-stu-id="307af-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="307af-111">D3DX \_ NORMALMAP \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="307af-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="307af-112">O mesmo que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.</span><span class="sxs-lookup"><span data-stu-id="307af-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="307af-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="307af-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="307af-114">Inverte a direção de cada normal.</span><span class="sxs-lookup"><span data-stu-id="307af-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="307af-115">OCLUSÃO DE COMPUTAÇÃO DE NORMALMAP D3DX \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="307af-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="307af-116">Calcula o termo de oclusão por pixel e o codifica no alfa.</span><span class="sxs-lookup"><span data-stu-id="307af-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="307af-117">Um alfa de 1 significa que o pixel não é obscurecido de nenhuma maneira, e um alfa de 0 significa que o pixel está completamente obscurecido.</span><span class="sxs-lookup"><span data-stu-id="307af-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="307af-118">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="307af-118">Constant Information</span></span>



| <span data-ttu-id="307af-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="307af-119">Requirement</span></span>                         | <span data-ttu-id="307af-120">Valor</span><span class="sxs-lookup"><span data-stu-id="307af-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="307af-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="307af-121">Header</span></span>                   | <span data-ttu-id="307af-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="307af-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="307af-123">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="307af-123">Minimum operating system</span></span> | <span data-ttu-id="307af-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="307af-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="307af-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="307af-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307af-126">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="307af-126">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="307af-127">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="307af-127">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



