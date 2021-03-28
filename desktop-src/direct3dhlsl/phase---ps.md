---
title: fase-PS
description: A instrução Phase marca a transição entre a fase 1 e a fase 2. Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador da fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006917"
---
# <a name="phase---ps"></a><span data-ttu-id="bc9f7-104">fase-PS</span><span class="sxs-lookup"><span data-stu-id="bc9f7-104">phase - ps</span></span>

<span data-ttu-id="bc9f7-105">A instrução Phase marca a transição entre a fase 1 e a fase 2.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="bc9f7-106">Se nenhuma instrução de fase estiver presente, o sombreador inteiro será executado como se fosse um sombreador da fase 2.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="bc9f7-107">Esta instrução aplica-se somente à versão 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9f7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc9f7-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="bc9f7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc9f7-109">Remarks</span></span>



| <span data-ttu-id="bc9f7-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bc9f7-110">Pixel shader versions</span></span> | <span data-ttu-id="bc9f7-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="bc9f7-111">1\_1</span></span> | <span data-ttu-id="bc9f7-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="bc9f7-112">1\_2</span></span> | <span data-ttu-id="bc9f7-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bc9f7-113">1\_3</span></span> | <span data-ttu-id="bc9f7-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="bc9f7-114">1\_4</span></span> | <span data-ttu-id="bc9f7-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc9f7-115">2\_0</span></span> | <span data-ttu-id="bc9f7-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bc9f7-116">2\_x</span></span> | <span data-ttu-id="bc9f7-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc9f7-117">2\_sw</span></span> | <span data-ttu-id="bc9f7-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc9f7-118">3\_0</span></span> | <span data-ttu-id="bc9f7-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc9f7-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bc9f7-120">fase</span><span class="sxs-lookup"><span data-stu-id="bc9f7-120">phase</span></span>                 |      |      |      | <span data-ttu-id="bc9f7-121">x</span><span class="sxs-lookup"><span data-stu-id="bc9f7-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="bc9f7-122">As instruções do sombreador que ocorrem antes da instrução Phase são instruções da fase 1.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="bc9f7-123">Todas as outras instruções são instruções da fase 2.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="bc9f7-124">Tendo duas fases para obter instruções, o número máximo de instruções por sombreador é aumentado.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="bc9f7-125">O efeito coverso da transição de fase é que o componente alfa de [registros temporários](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) não persiste na transição.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="bc9f7-126">Em outras palavras, o componente alfa deve ser reinicializado após a instrução phase.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="bc9f7-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bc9f7-127">Example</span></span>

<span data-ttu-id="bc9f7-128">Este exemplo mostra como agrupar instruções como instruções da fase 1 ou 2 em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="bc9f7-129">A instrução Phase também é normalmente chamada de marcador de fase porque marca a transição entre as instruções da fase 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="bc9f7-130">Em um \_ sombreador de 4 pixels de versão 1, se o marcador de fase não estiver presente, o sombreador será executado como se ele fosse executado na fase 2.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="bc9f7-131">Isso é importante porque há diferenças entre as instruções da fase 1 e 2 e o registro da disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="bc9f7-132">As diferenças são indicadas em toda a seção de referência.</span><span class="sxs-lookup"><span data-stu-id="bc9f7-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="bc9f7-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc9f7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc9f7-134">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bc9f7-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




