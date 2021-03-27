---
title: Objetos do Shader Model 5,1
description: Os seguintes objetos foram adicionados ao modelo do sombreador 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294206"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="3b271-103">Objetos do Shader Model 5,1</span><span class="sxs-lookup"><span data-stu-id="3b271-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="3b271-104">Os seguintes objetos foram adicionados ao modelo do sombreador 5,1.</span><span class="sxs-lookup"><span data-stu-id="3b271-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="3b271-105">Para as [exibições de ordem de rasterizador](/windows/desktop/direct3d11/rasterizer-order-views) (disponíveis no D3D 11.3 e D3D12), os seguintes objetos são novos e são permitidos somente no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="3b271-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="3b271-106">Observe que os métodos aos quais eles dão suporte são idênticos aos objetos UAV correspondentes.</span><span class="sxs-lookup"><span data-stu-id="3b271-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3b271-107">Objeto rasterizador</span><span class="sxs-lookup"><span data-stu-id="3b271-107">Rasterizer Object</span></span>                  | <span data-ttu-id="3b271-108">Objeto UAV</span><span class="sxs-lookup"><span data-stu-id="3b271-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="3b271-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="3b271-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="3b271-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="3b271-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="3b271-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="3b271-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="3b271-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="3b271-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="3b271-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3b271-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="3b271-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="3b271-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="3b271-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="3b271-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="3b271-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="3b271-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="3b271-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="3b271-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="3b271-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="3b271-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="3b271-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="3b271-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="3b271-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="3b271-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="3b271-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="3b271-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="3b271-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="3b271-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="3b271-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="3b271-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="3b271-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="3b271-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="3b271-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b271-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b271-126">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="3b271-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="3b271-127">Recursos do HLSL Shader Model 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b271-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 