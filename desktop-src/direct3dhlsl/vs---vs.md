---
title: vs
description: Esta instrução especifica o número de versão do sombreador. Essa instrução funciona em todas as versões de sombreador.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365281"
---
# <a name="vs"></a><span data-ttu-id="b865c-104">vs</span><span class="sxs-lookup"><span data-stu-id="b865c-104">vs</span></span>

<span data-ttu-id="b865c-105">Esta instrução especifica o número de versão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b865c-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="b865c-106">Essa instrução funciona em todas as versões de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b865c-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b865c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b865c-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="b865c-108">Argumentos de entrada</span><span class="sxs-lookup"><span data-stu-id="b865c-108">Input Arguments</span></span>

<span data-ttu-id="b865c-109">Os argumentos de entrada contêm um único número de versão principal com um único número de subversão.</span><span class="sxs-lookup"><span data-stu-id="b865c-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="b865c-110">As combinações permitidas são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b865c-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="b865c-111">Versões principais</span><span class="sxs-lookup"><span data-stu-id="b865c-111">Main versions</span></span> | <span data-ttu-id="b865c-112">Sub-versões</span><span class="sxs-lookup"><span data-stu-id="b865c-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="b865c-113">1</span><span class="sxs-lookup"><span data-stu-id="b865c-113">1</span></span>             | <span data-ttu-id="b865c-114">1</span><span class="sxs-lookup"><span data-stu-id="b865c-114">1</span></span>                              |
| <span data-ttu-id="b865c-115">2</span><span class="sxs-lookup"><span data-stu-id="b865c-115">2</span></span>             | <span data-ttu-id="b865c-116">0, SW (software), x (estendido)</span><span class="sxs-lookup"><span data-stu-id="b865c-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="b865c-117">3</span><span class="sxs-lookup"><span data-stu-id="b865c-117">3</span></span>             | <span data-ttu-id="b865c-118">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="b865c-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="b865c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b865c-119">Remarks</span></span>



| <span data-ttu-id="b865c-120">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b865c-120">Vertex shader versions</span></span> | <span data-ttu-id="b865c-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="b865c-121">1\_1</span></span> | <span data-ttu-id="b865c-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b865c-122">2\_0</span></span> | <span data-ttu-id="b865c-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b865c-123">2\_x</span></span> | <span data-ttu-id="b865c-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b865c-124">2\_sw</span></span> | <span data-ttu-id="b865c-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b865c-125">3\_0</span></span> | <span data-ttu-id="b865c-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b865c-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b865c-127">vs</span><span class="sxs-lookup"><span data-stu-id="b865c-127">vs</span></span>                     | <span data-ttu-id="b865c-128">x</span><span class="sxs-lookup"><span data-stu-id="b865c-128">x</span></span>    | <span data-ttu-id="b865c-129">x</span><span class="sxs-lookup"><span data-stu-id="b865c-129">x</span></span>    | <span data-ttu-id="b865c-130">x</span><span class="sxs-lookup"><span data-stu-id="b865c-130">x</span></span>    | <span data-ttu-id="b865c-131">x</span><span class="sxs-lookup"><span data-stu-id="b865c-131">x</span></span>     | <span data-ttu-id="b865c-132">x</span><span class="sxs-lookup"><span data-stu-id="b865c-132">x</span></span>    | <span data-ttu-id="b865c-133">x</span><span class="sxs-lookup"><span data-stu-id="b865c-133">x</span></span>     |



 

<span data-ttu-id="b865c-134">Essa instrução deve ser a primeira instrução que não seja de comentário em um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b865c-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="b865c-135">Essa instrução tem suporte em todas as versões de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b865c-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="b865c-136">As versões aceleradas por hardware do software (versões sem \_ SW no número de versão) podem processar vértices com accelearation de hardware ou usar o processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="b865c-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="b865c-137">Versões de software (versões com \_ SW no número de versão) processam vértices somente com software.</span><span class="sxs-lookup"><span data-stu-id="b865c-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="b865c-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b865c-138">Examples</span></span>

<span data-ttu-id="b865c-139">Este exemplo parcial declara um sombreador de vértice da versão 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="b865c-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="b865c-140">Este exemplo parcial declara um sombreador de vértice de software da versão 2.</span><span class="sxs-lookup"><span data-stu-id="b865c-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="b865c-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b865c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b865c-142">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b865c-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




