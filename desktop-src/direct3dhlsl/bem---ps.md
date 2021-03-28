---
title: Bem-PS
description: Aplicar um ambiente de relevo falso – transformação de mapa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365253"
---
# <a name="bem---ps"></a><span data-ttu-id="57d5e-103">Bem-PS</span><span class="sxs-lookup"><span data-stu-id="57d5e-103">bem - ps</span></span>

<span data-ttu-id="57d5e-104">Aplicar um ambiente de relevo falso – transformação de mapa.</span><span class="sxs-lookup"><span data-stu-id="57d5e-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57d5e-105">Syntax</span></span>



| <span data-ttu-id="57d5e-106">Bem DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="57d5e-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="57d5e-107">onde</span><span class="sxs-lookup"><span data-stu-id="57d5e-107">where</span></span>

-   <span data-ttu-id="57d5e-108">DST. RG DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="57d5e-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="57d5e-109">A máscara de gravação do componente vermelho e verde deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="57d5e-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="57d5e-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="57d5e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="57d5e-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="57d5e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d5e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="57d5e-112">Remarks</span></span>



| <span data-ttu-id="57d5e-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="57d5e-113">Pixel shader versions</span></span> | <span data-ttu-id="57d5e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="57d5e-114">1\_1</span></span> | <span data-ttu-id="57d5e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="57d5e-115">1\_2</span></span> | <span data-ttu-id="57d5e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="57d5e-116">1\_3</span></span> | <span data-ttu-id="57d5e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="57d5e-117">1\_4</span></span> | <span data-ttu-id="57d5e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57d5e-118">2\_0</span></span> | <span data-ttu-id="57d5e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="57d5e-119">2\_x</span></span> | <span data-ttu-id="57d5e-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="57d5e-120">2\_sw</span></span> | <span data-ttu-id="57d5e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57d5e-121">3\_0</span></span> | <span data-ttu-id="57d5e-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="57d5e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="57d5e-123">bem</span><span class="sxs-lookup"><span data-stu-id="57d5e-123">bem</span></span>                   |      |      |      | <span data-ttu-id="57d5e-124">x</span><span class="sxs-lookup"><span data-stu-id="57d5e-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="57d5e-125">Essa instrução executa o cálculo a seguir.</span><span class="sxs-lookup"><span data-stu-id="57d5e-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="57d5e-126">Regras para usar bem:</span><span class="sxs-lookup"><span data-stu-id="57d5e-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="57d5e-127">Bem deve aparecer na primeira fase de um sombreador (ou seja, antes de um marcador de fase).</span><span class="sxs-lookup"><span data-stu-id="57d5e-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="57d5e-128">Bem consome dois slots de instrução aritméticos.</span><span class="sxs-lookup"><span data-stu-id="57d5e-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="57d5e-129">Somente um uso desta instrução é permitido por sombreador.</span><span class="sxs-lookup"><span data-stu-id="57d5e-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="57d5e-130">Writemask de destino deve ser. RG/.XY.</span><span class="sxs-lookup"><span data-stu-id="57d5e-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="57d5e-131">Esta instrução não pode ser emitida em conjunto.</span><span class="sxs-lookup"><span data-stu-id="57d5e-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="57d5e-132">Além da restrição que a máscara de gravação de destino é. RG, os modificadores nos modificadores de origem src0, src1 e instrução são irrestrito.</span><span class="sxs-lookup"><span data-stu-id="57d5e-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="57d5e-133">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="57d5e-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="57d5e-134">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="57d5e-134">Minimum operating system</span></span> | <span data-ttu-id="57d5e-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="57d5e-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="57d5e-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57d5e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57d5e-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="57d5e-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




