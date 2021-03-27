---
title: Mova-vs
description: Mover dados de um ponto flutuante registrar para o registro de endereço, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967131"
---
# <a name="mova---vs"></a><span data-ttu-id="efe81-103">Mova-vs</span><span class="sxs-lookup"><span data-stu-id="efe81-103">mova - vs</span></span>

<span data-ttu-id="efe81-104">Mover dados de um ponto flutuante registrar para o [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="efe81-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efe81-105">Syntax</span></span>



| <span data-ttu-id="efe81-106">Mova DST, src</span><span class="sxs-lookup"><span data-stu-id="efe81-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="efe81-107">onde</span><span class="sxs-lookup"><span data-stu-id="efe81-107">where</span></span>

-   <span data-ttu-id="efe81-108">o DST deve ser o [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="efe81-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="efe81-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="efe81-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe81-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe81-110">Remarks</span></span>



| <span data-ttu-id="efe81-111">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="efe81-111">Vertex shader versions</span></span> | <span data-ttu-id="efe81-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="efe81-112">1\_1</span></span> | <span data-ttu-id="efe81-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efe81-113">2\_0</span></span> | <span data-ttu-id="efe81-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="efe81-114">2\_x</span></span> | <span data-ttu-id="efe81-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efe81-115">2\_sw</span></span> | <span data-ttu-id="efe81-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efe81-116">3\_0</span></span> | <span data-ttu-id="efe81-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efe81-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="efe81-118">mova</span><span class="sxs-lookup"><span data-stu-id="efe81-118">mova</span></span>                   |      | <span data-ttu-id="efe81-119">x</span><span class="sxs-lookup"><span data-stu-id="efe81-119">x</span></span>    | <span data-ttu-id="efe81-120">x</span><span class="sxs-lookup"><span data-stu-id="efe81-120">x</span></span>    | <span data-ttu-id="efe81-121">x</span><span class="sxs-lookup"><span data-stu-id="efe81-121">x</span></span>     | <span data-ttu-id="efe81-122">x</span><span class="sxs-lookup"><span data-stu-id="efe81-122">x</span></span>    | <span data-ttu-id="efe81-123">x</span><span class="sxs-lookup"><span data-stu-id="efe81-123">x</span></span>     |



 

<span data-ttu-id="efe81-124">Move os dados de ponto flutuante para um registro de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="efe81-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="efe81-125">Os valores são convertidos do ponto flutuante usando o arredondamento para o mais próximo.</span><span class="sxs-lookup"><span data-stu-id="efe81-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="efe81-126">O registro de endereço é o único registro de destino permitido.</span><span class="sxs-lookup"><span data-stu-id="efe81-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="efe81-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="efe81-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="efe81-128">Para as versões 2 \_ x e posteriores, o registro de endereço é um vetor de componente.</span><span class="sxs-lookup"><span data-stu-id="efe81-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="efe81-129">Portanto, qualquer máscara de gravação é permitida.</span><span class="sxs-lookup"><span data-stu-id="efe81-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="efe81-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efe81-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe81-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="efe81-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




