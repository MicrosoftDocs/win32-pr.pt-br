---
title: sgn-vs
description: Computa o sinal da entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365236"
---
# <a name="sgn---vs"></a><span data-ttu-id="28b93-103">sgn-vs</span><span class="sxs-lookup"><span data-stu-id="28b93-103">sgn - vs</span></span>

<span data-ttu-id="28b93-104">Computa o sinal da entrada.</span><span class="sxs-lookup"><span data-stu-id="28b93-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b93-105">Syntax</span></span>



| <span data-ttu-id="28b93-106">sgn DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="28b93-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="28b93-107">onde</span><span class="sxs-lookup"><span data-stu-id="28b93-107">where</span></span>

-   <span data-ttu-id="28b93-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="28b93-108">dst is the destination register.</span></span>
-   <span data-ttu-id="28b93-109">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="28b93-109">src0 is a source register.</span></span>
-   <span data-ttu-id="28b93-110">src1 é um registro temporário que contém resultados intermediários.</span><span class="sxs-lookup"><span data-stu-id="28b93-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="28b93-111">Após a execução, os conteúdos são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="28b93-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="28b93-112">src2 é um registro temporário que contém resultados intermediários.</span><span class="sxs-lookup"><span data-stu-id="28b93-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="28b93-113">Após a execução, os conteúdos são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="28b93-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b93-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="28b93-114">Remarks</span></span>



| <span data-ttu-id="28b93-115">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="28b93-115">Vertex shader versions</span></span> | <span data-ttu-id="28b93-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="28b93-116">1\_1</span></span> | <span data-ttu-id="28b93-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28b93-117">2\_0</span></span> | <span data-ttu-id="28b93-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28b93-118">2\_x</span></span> | <span data-ttu-id="28b93-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28b93-119">2\_sw</span></span> | <span data-ttu-id="28b93-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28b93-120">3\_0</span></span> | <span data-ttu-id="28b93-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28b93-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="28b93-122">Sgn</span><span class="sxs-lookup"><span data-stu-id="28b93-122">sgn</span></span>                    |      | <span data-ttu-id="28b93-123">x</span><span class="sxs-lookup"><span data-stu-id="28b93-123">x</span></span>    | <span data-ttu-id="28b93-124">x</span><span class="sxs-lookup"><span data-stu-id="28b93-124">x</span></span>    | <span data-ttu-id="28b93-125">x</span><span class="sxs-lookup"><span data-stu-id="28b93-125">x</span></span>     | <span data-ttu-id="28b93-126">x</span><span class="sxs-lookup"><span data-stu-id="28b93-126">x</span></span>    | <span data-ttu-id="28b93-127">x</span><span class="sxs-lookup"><span data-stu-id="28b93-127">x</span></span>     |



 

<span data-ttu-id="28b93-128">Essa instrução funciona conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="28b93-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="28b93-129">src1 e src2 devem ser diferentes s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md).</span><span class="sxs-lookup"><span data-stu-id="28b93-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28b93-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28b93-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28b93-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="28b93-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




