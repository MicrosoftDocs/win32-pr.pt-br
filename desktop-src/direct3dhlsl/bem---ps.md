---
title: bem - ps
description: Aplicar uma transformação de mapa de ambiente de aumento falso.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129925"
---
# <a name="bem---ps"></a><span data-ttu-id="e3b00-103">bem - ps</span><span class="sxs-lookup"><span data-stu-id="e3b00-103">bem - ps</span></span>

<span data-ttu-id="e3b00-104">Aplicar uma transformação de mapa de ambiente de aumento falso.</span><span class="sxs-lookup"><span data-stu-id="e3b00-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b00-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3b00-105">Syntax</span></span>



| <span data-ttu-id="e3b00-106">bem dst.rg, src0, src1</span><span class="sxs-lookup"><span data-stu-id="e3b00-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="e3b00-107">onde</span><span class="sxs-lookup"><span data-stu-id="e3b00-107">where</span></span>

-   <span data-ttu-id="e3b00-108">dst.rg dst é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e3b00-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="e3b00-109">A máscara de gravação do componente vermelho e verde deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="e3b00-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="e3b00-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="e3b00-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e3b00-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="e3b00-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b00-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3b00-112">Remarks</span></span>



| <span data-ttu-id="e3b00-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e3b00-113">Pixel shader versions</span></span> | <span data-ttu-id="e3b00-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e3b00-114">1\_1</span></span> | <span data-ttu-id="e3b00-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e3b00-115">1\_2</span></span> | <span data-ttu-id="e3b00-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e3b00-116">1\_3</span></span> | <span data-ttu-id="e3b00-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e3b00-117">1\_4</span></span> | <span data-ttu-id="e3b00-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3b00-118">2\_0</span></span> | <span data-ttu-id="e3b00-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3b00-119">2\_x</span></span> | <span data-ttu-id="e3b00-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3b00-120">2\_sw</span></span> | <span data-ttu-id="e3b00-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3b00-121">3\_0</span></span> | <span data-ttu-id="e3b00-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3b00-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e3b00-123">bem</span><span class="sxs-lookup"><span data-stu-id="e3b00-123">bem</span></span>                   |      |      |      | <span data-ttu-id="e3b00-124">x</span><span class="sxs-lookup"><span data-stu-id="e3b00-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="e3b00-125">Essa instrução executa o cálculo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3b00-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="e3b00-126">Regras para usar bem:</span><span class="sxs-lookup"><span data-stu-id="e3b00-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="e3b00-127">bem deve aparecer na primeira fase de um sombreador (ou seja, antes de um marcador de fase).</span><span class="sxs-lookup"><span data-stu-id="e3b00-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="e3b00-128">bem consome dois slots de instrução aritmética.</span><span class="sxs-lookup"><span data-stu-id="e3b00-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="e3b00-129">Somente um uso dessa instrução é permitido por sombreador.</span><span class="sxs-lookup"><span data-stu-id="e3b00-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="e3b00-130">A máscara de gravação de destino deve ser .rg /.xy.</span><span class="sxs-lookup"><span data-stu-id="e3b00-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="e3b00-131">Essa instrução não pode ser co-emitida.</span><span class="sxs-lookup"><span data-stu-id="e3b00-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="e3b00-132">Além da restrição de que a máscara de gravação de destino seja .rg, os modificadores em src0 de origem, src1 e modificadores de instrução não são restritos.</span><span class="sxs-lookup"><span data-stu-id="e3b00-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="e3b00-133">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="e3b00-133">Instruction Information</span></span>



| <span data-ttu-id="e3b00-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b00-134">Requirement</span></span>                         | <span data-ttu-id="e3b00-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e3b00-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e3b00-136">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="e3b00-136">Minimum operating system</span></span> | <span data-ttu-id="e3b00-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e3b00-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3b00-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3b00-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3b00-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e3b00-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




