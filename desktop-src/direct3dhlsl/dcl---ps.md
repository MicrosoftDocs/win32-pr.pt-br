---
title: DCL-(SM2, SM3-PS ASM)
description: Declare um registro de entrada de sombreador de pixel.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365259"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="b0e8a-103">DCL-(SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="b0e8a-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="b0e8a-104">Declare um registro de entrada de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b0e8a-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e8a-105">Syntax</span></span>



|                           |
|---------------------------|
| <span data-ttu-id="b0e8a-106">\[ \_ máscara de \] dest PP \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="b0e8a-106">dcl\[\_pp\] dest\[.mask\]</span></span> |



 

<span data-ttu-id="b0e8a-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="b0e8a-107">Where:</span></span>

-   <span data-ttu-id="b0e8a-108">\[\_PP \] é precisão parcial opcional.</span><span class="sxs-lookup"><span data-stu-id="b0e8a-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="b0e8a-109">Consulte [precisão parcial](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="b0e8a-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="b0e8a-110">dest é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b0e8a-110">dest is a destination register.</span></span> <span data-ttu-id="b0e8a-111">Ele deve ser um [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) ou um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).</span><span class="sxs-lookup"><span data-stu-id="b0e8a-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="b0e8a-112">\[. Mask \] é uma máscara de gravação opcional que controla quais componentes do registro de destino podem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="b0e8a-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="b0e8a-113">Consulte [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="b0e8a-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e8a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0e8a-114">Remarks</span></span>



| <span data-ttu-id="b0e8a-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0e8a-115">Pixel shader versions</span></span> | <span data-ttu-id="b0e8a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="b0e8a-116">1\_1</span></span> | <span data-ttu-id="b0e8a-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="b0e8a-117">1\_2</span></span> | <span data-ttu-id="b0e8a-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0e8a-118">1\_3</span></span> | <span data-ttu-id="b0e8a-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0e8a-119">1\_4</span></span> | <span data-ttu-id="b0e8a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0e8a-120">2\_0</span></span> | <span data-ttu-id="b0e8a-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-121">2\_x</span></span> | <span data-ttu-id="b0e8a-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0e8a-122">2\_sw</span></span> | <span data-ttu-id="b0e8a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0e8a-123">3\_0</span></span> | <span data-ttu-id="b0e8a-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0e8a-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b0e8a-125">DCL</span><span class="sxs-lookup"><span data-stu-id="b0e8a-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="b0e8a-126">x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-126">x</span></span>    | <span data-ttu-id="b0e8a-127">x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-127">x</span></span>    | <span data-ttu-id="b0e8a-128">x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-128">x</span></span>     | <span data-ttu-id="b0e8a-129">x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-129">x</span></span>    | <span data-ttu-id="b0e8a-130">x</span><span class="sxs-lookup"><span data-stu-id="b0e8a-130">x</span></span>     |



 

<span data-ttu-id="b0e8a-131">Todas as instruções de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="b0e8a-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0e8a-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0e8a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e8a-133">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0e8a-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




