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
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994743"
---
# <a name="abs---vs"></a><span data-ttu-id="ec2fc-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="ec2fc-104">abs - vs</span></span>

<span data-ttu-id="ec2fc-105">Calcula o valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="ec2fc-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec2fc-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="ec2fc-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="ec2fc-107">abs dst, src</span></span> |



 

<span data-ttu-id="ec2fc-108">onde</span><span class="sxs-lookup"><span data-stu-id="ec2fc-108">where</span></span>

-   <span data-ttu-id="ec2fc-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ec2fc-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ec2fc-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="ec2fc-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2fc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec2fc-111">Remarks</span></span>



| <span data-ttu-id="ec2fc-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ec2fc-112">Vertex shader versions</span></span> | <span data-ttu-id="ec2fc-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ec2fc-113">1\_1</span></span> | <span data-ttu-id="ec2fc-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec2fc-114">2\_0</span></span> | <span data-ttu-id="ec2fc-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-115">2\_x</span></span> | <span data-ttu-id="ec2fc-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec2fc-116">2\_sw</span></span> | <span data-ttu-id="ec2fc-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec2fc-117">3\_0</span></span> | <span data-ttu-id="ec2fc-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec2fc-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ec2fc-119">abs</span><span class="sxs-lookup"><span data-stu-id="ec2fc-119">abs</span></span>                    |      | <span data-ttu-id="ec2fc-120">x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-120">x</span></span>    | <span data-ttu-id="ec2fc-121">x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-121">x</span></span>    | <span data-ttu-id="ec2fc-122">x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-122">x</span></span>     | <span data-ttu-id="ec2fc-123">x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-123">x</span></span>    | <span data-ttu-id="ec2fc-124">x</span><span class="sxs-lookup"><span data-stu-id="ec2fc-124">x</span></span>     |



 

<span data-ttu-id="ec2fc-125">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="ec2fc-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="ec2fc-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec2fc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec2fc-127">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ec2fc-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




