---
title: ps
description: Essa instrução especifica o número de versão do sombreador e funciona em todas as versões do sombreador.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988611"
---
# <a name="ps"></a><span data-ttu-id="34e47-103">ps</span><span class="sxs-lookup"><span data-stu-id="34e47-103">ps</span></span>

<span data-ttu-id="34e47-104">Essa instrução especifica o número de versão do sombreador e funciona em todas as versões do sombreador.</span><span class="sxs-lookup"><span data-stu-id="34e47-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e47-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="34e47-106">Argumentos de entrada</span><span class="sxs-lookup"><span data-stu-id="34e47-106">Input Arguments</span></span>

<span data-ttu-id="34e47-107">Os argumentos de entrada contêm um único número de versão principal com um único número de subversão.</span><span class="sxs-lookup"><span data-stu-id="34e47-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="34e47-108">As combinações permitidas são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34e47-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="34e47-109">Versões principais</span><span class="sxs-lookup"><span data-stu-id="34e47-109">Main versions</span></span> | <span data-ttu-id="34e47-110">Sub-versões</span><span class="sxs-lookup"><span data-stu-id="34e47-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="34e47-111">1</span><span class="sxs-lookup"><span data-stu-id="34e47-111">1</span></span>             | <span data-ttu-id="34e47-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="34e47-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="34e47-113">2</span><span class="sxs-lookup"><span data-stu-id="34e47-113">2</span></span>             | <span data-ttu-id="34e47-114">0, x (estendido), SW (software)</span><span class="sxs-lookup"><span data-stu-id="34e47-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="34e47-115">3</span><span class="sxs-lookup"><span data-stu-id="34e47-115">3</span></span>             | <span data-ttu-id="34e47-116">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="34e47-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="34e47-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="34e47-117">Remarks</span></span>



| <span data-ttu-id="34e47-118">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34e47-118">Pixel shader versions</span></span> | <span data-ttu-id="34e47-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="34e47-119">1\_1</span></span> | <span data-ttu-id="34e47-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="34e47-120">1\_2</span></span> | <span data-ttu-id="34e47-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34e47-121">1\_3</span></span> | <span data-ttu-id="34e47-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="34e47-122">1\_4</span></span> | <span data-ttu-id="34e47-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34e47-123">2\_0</span></span> | <span data-ttu-id="34e47-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="34e47-124">2\_x</span></span> | <span data-ttu-id="34e47-125">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34e47-125">2\_sw</span></span> | <span data-ttu-id="34e47-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34e47-126">3\_0</span></span> | <span data-ttu-id="34e47-127">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34e47-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="34e47-128">ps</span><span class="sxs-lookup"><span data-stu-id="34e47-128">ps</span></span>                    | <span data-ttu-id="34e47-129">x</span><span class="sxs-lookup"><span data-stu-id="34e47-129">x</span></span>    | <span data-ttu-id="34e47-130">x</span><span class="sxs-lookup"><span data-stu-id="34e47-130">x</span></span>    | <span data-ttu-id="34e47-131">x</span><span class="sxs-lookup"><span data-stu-id="34e47-131">x</span></span>    | <span data-ttu-id="34e47-132">x</span><span class="sxs-lookup"><span data-stu-id="34e47-132">x</span></span>    | <span data-ttu-id="34e47-133">x</span><span class="sxs-lookup"><span data-stu-id="34e47-133">x</span></span>    | <span data-ttu-id="34e47-134">x</span><span class="sxs-lookup"><span data-stu-id="34e47-134">x</span></span>    | <span data-ttu-id="34e47-135">x</span><span class="sxs-lookup"><span data-stu-id="34e47-135">x</span></span>     | <span data-ttu-id="34e47-136">x</span><span class="sxs-lookup"><span data-stu-id="34e47-136">x</span></span>    | <span data-ttu-id="34e47-137">x</span><span class="sxs-lookup"><span data-stu-id="34e47-137">x</span></span>     |



 

<span data-ttu-id="34e47-138">Essa instrução deve ser a primeira instrução que não seja de comentário em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="34e47-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="34e47-139">As versões aceleradas por hardware do software (versões sem \_ SW no número de versão) podem processar vértices com accelearation de hardware ou usar o processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="34e47-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="34e47-140">Versões de software (versões com \_ SW no número de versão) processam vértices somente com software.</span><span class="sxs-lookup"><span data-stu-id="34e47-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="34e47-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34e47-141">Examples</span></span>

<span data-ttu-id="34e47-142">Este exemplo parcial declara um sombreador de pixel da versão 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="34e47-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="34e47-143">Este exemplo parcial declara um \_ sombreador de 4 pixels da versão 1.</span><span class="sxs-lookup"><span data-stu-id="34e47-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="34e47-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34e47-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34e47-145">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34e47-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




