---
title: MOV-vs
description: Mover dados de ponto flutuante entre os registros.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638886"
---
# <a name="mov---vs"></a><span data-ttu-id="94b0d-103">MOV-vs</span><span class="sxs-lookup"><span data-stu-id="94b0d-103">mov - vs</span></span>

<span data-ttu-id="94b0d-104">Mover dados de ponto flutuante entre os registros.</span><span class="sxs-lookup"><span data-stu-id="94b0d-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b0d-105">Syntax</span></span>



| <span data-ttu-id="94b0d-106">MOV DST, src</span><span class="sxs-lookup"><span data-stu-id="94b0d-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="94b0d-107">onde</span><span class="sxs-lookup"><span data-stu-id="94b0d-107">where</span></span>

-   <span data-ttu-id="94b0d-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="94b0d-108">dst is the destination register.</span></span>
-   <span data-ttu-id="94b0d-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="94b0d-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b0d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="94b0d-110">Remarks</span></span>



| <span data-ttu-id="94b0d-111">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="94b0d-111">Vertex shader versions</span></span> | <span data-ttu-id="94b0d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="94b0d-112">1\_1</span></span> | <span data-ttu-id="94b0d-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b0d-113">2\_0</span></span> | <span data-ttu-id="94b0d-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="94b0d-114">2\_x</span></span> | <span data-ttu-id="94b0d-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b0d-115">2\_sw</span></span> | <span data-ttu-id="94b0d-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b0d-116">3\_0</span></span> | <span data-ttu-id="94b0d-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b0d-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="94b0d-118">média</span><span class="sxs-lookup"><span data-stu-id="94b0d-118">mov</span></span>                    | <span data-ttu-id="94b0d-119">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-119">x</span></span>    | <span data-ttu-id="94b0d-120">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-120">x</span></span>    | <span data-ttu-id="94b0d-121">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-121">x</span></span>    | <span data-ttu-id="94b0d-122">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-122">x</span></span>     | <span data-ttu-id="94b0d-123">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-123">x</span></span>    | <span data-ttu-id="94b0d-124">x</span><span class="sxs-lookup"><span data-stu-id="94b0d-124">x</span></span>     |



 

<span data-ttu-id="94b0d-125">Pode ser usado para dados de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="94b0d-125">Can be used for floating point data.</span></span> <span data-ttu-id="94b0d-126">Para a versão vs \_ 1 \_ 1, ele também pode ser usado para gravar o registro de endereço.</span><span class="sxs-lookup"><span data-stu-id="94b0d-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="94b0d-127">Quando usado para atualizar os registros de endereço, os valores são convertidos do ponto flutuante usando o arredondamento para o mais próximo.</span><span class="sxs-lookup"><span data-stu-id="94b0d-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="94b0d-128">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="94b0d-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="94b0d-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94b0d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b0d-130">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="94b0d-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




