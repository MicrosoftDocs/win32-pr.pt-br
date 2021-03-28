---
title: ABS-vs
description: Calcula o valor absoluto. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172616"
---
# <a name="abs---vs"></a><span data-ttu-id="a1890-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="a1890-104">abs - vs</span></span>

<span data-ttu-id="a1890-105">Calcula o valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="a1890-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1890-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1890-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="a1890-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="a1890-107">abs dst, src</span></span> |



 

<span data-ttu-id="a1890-108">onde</span><span class="sxs-lookup"><span data-stu-id="a1890-108">where</span></span>

-   <span data-ttu-id="a1890-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a1890-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a1890-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="a1890-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1890-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1890-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1890-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a1890-112">Vertex shader versions</span></span> | <span data-ttu-id="a1890-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1890-113">1\_1</span></span> | <span data-ttu-id="a1890-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1890-114">2\_0</span></span> | <span data-ttu-id="a1890-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1890-115">2\_x</span></span> | <span data-ttu-id="a1890-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1890-116">2\_sw</span></span> | <span data-ttu-id="a1890-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1890-117">3\_0</span></span> | <span data-ttu-id="a1890-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1890-118">3\_sw</span></span> |
| <span data-ttu-id="a1890-119">abs</span><span class="sxs-lookup"><span data-stu-id="a1890-119">abs</span></span>                    |      | <span data-ttu-id="a1890-120">x</span><span class="sxs-lookup"><span data-stu-id="a1890-120">x</span></span>    | <span data-ttu-id="a1890-121">x</span><span class="sxs-lookup"><span data-stu-id="a1890-121">x</span></span>    | <span data-ttu-id="a1890-122">x</span><span class="sxs-lookup"><span data-stu-id="a1890-122">x</span></span>     | <span data-ttu-id="a1890-123">x</span><span class="sxs-lookup"><span data-stu-id="a1890-123">x</span></span>    | <span data-ttu-id="a1890-124">x</span><span class="sxs-lookup"><span data-stu-id="a1890-124">x</span></span>     |



 

<span data-ttu-id="a1890-125">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="a1890-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="a1890-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1890-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1890-127">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a1890-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




