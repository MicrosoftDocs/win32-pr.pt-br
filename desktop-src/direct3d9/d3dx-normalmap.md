---
description: Constantes de geração de mapas normais.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f76b6afe6eb68e8ddbc3ca28085861a518effc
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996323"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="f8f99-103">D3DX \_ NormalMap</span><span class="sxs-lookup"><span data-stu-id="f8f99-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="f8f99-104">Constantes de geração de mapas normais.</span><span class="sxs-lookup"><span data-stu-id="f8f99-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="f8f99-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="f8f99-105">\#define</span></span>                            | <span data-ttu-id="f8f99-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8f99-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f99-107">D3DX \_ NormalMap \_ Mirror \_ U</span><span class="sxs-lookup"><span data-stu-id="f8f99-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="f8f99-108">Indica que os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="f8f99-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f8f99-109">D3DX \_ NormalMap \_ Mirror \_ V</span><span class="sxs-lookup"><span data-stu-id="f8f99-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="f8f99-110">Indica que os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="f8f99-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f8f99-111">D3DX \_ NormalMap \_ Mirror</span><span class="sxs-lookup"><span data-stu-id="f8f99-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="f8f99-112">O mesmo que especificar D3DX \_ NormalMap \_ espelho \_ U \| D3DX \_ NormalMap \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="f8f99-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="f8f99-113">D3DX \_ NormalMap \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="f8f99-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="f8f99-114">Inverte a direção de cada normal.</span><span class="sxs-lookup"><span data-stu-id="f8f99-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f8f99-115">D3DX \_ NormalMap \_ \_ oclusão Compute</span><span class="sxs-lookup"><span data-stu-id="f8f99-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="f8f99-116">Computa o termo oclusão por pixel e o codifica no Alpha.</span><span class="sxs-lookup"><span data-stu-id="f8f99-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="f8f99-117">Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significa que o pixel está completamente obscurecido.</span><span class="sxs-lookup"><span data-stu-id="f8f99-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="f8f99-118">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="f8f99-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f8f99-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8f99-119">Header</span></span>                   | <span data-ttu-id="f8f99-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="f8f99-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="f8f99-121">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="f8f99-121">Minimum operating system</span></span> | <span data-ttu-id="f8f99-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f8f99-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f8f99-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8f99-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8f99-124">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="f8f99-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="f8f99-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="f8f99-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



