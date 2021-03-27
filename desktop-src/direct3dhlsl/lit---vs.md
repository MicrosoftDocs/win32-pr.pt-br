---
title: aceso-vs
description: Fornece suporte parcial para iluminação ao calcular os coeficientes de iluminação de dois produtos de ponto e um expoente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967111"
---
# <a name="lit---vs"></a><span data-ttu-id="3a7c8-103">aceso-vs</span><span class="sxs-lookup"><span data-stu-id="3a7c8-103">lit - vs</span></span>

<span data-ttu-id="3a7c8-104">Fornece suporte parcial para iluminação ao calcular os coeficientes de iluminação de dois produtos de ponto e um expoente.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a7c8-105">Syntax</span></span>



| <span data-ttu-id="3a7c8-106">horário de verão aceso, src</span><span class="sxs-lookup"><span data-stu-id="3a7c8-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="3a7c8-107">onde</span><span class="sxs-lookup"><span data-stu-id="3a7c8-107">where</span></span>

-   <span data-ttu-id="3a7c8-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3a7c8-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a7c8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a7c8-110">Remarks</span></span>



| <span data-ttu-id="3a7c8-111">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3a7c8-111">Vertex shader versions</span></span> | <span data-ttu-id="3a7c8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3a7c8-112">1\_1</span></span> | <span data-ttu-id="3a7c8-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a7c8-113">2\_0</span></span> | <span data-ttu-id="3a7c8-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-114">2\_x</span></span> | <span data-ttu-id="3a7c8-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a7c8-115">2\_sw</span></span> | <span data-ttu-id="3a7c8-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a7c8-116">3\_0</span></span> | <span data-ttu-id="3a7c8-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a7c8-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3a7c8-118">aceso</span><span class="sxs-lookup"><span data-stu-id="3a7c8-118">lit</span></span>                    | <span data-ttu-id="3a7c8-119">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-119">x</span></span>    | <span data-ttu-id="3a7c8-120">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-120">x</span></span>    | <span data-ttu-id="3a7c8-121">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-121">x</span></span>    | <span data-ttu-id="3a7c8-122">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-122">x</span></span>     | <span data-ttu-id="3a7c8-123">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-123">x</span></span>    | <span data-ttu-id="3a7c8-124">x</span><span class="sxs-lookup"><span data-stu-id="3a7c8-124">x</span></span>     |



 

<span data-ttu-id="3a7c8-125">Presume-se que o vetor de origem contenha os valores mostrados no pseudocódigo a seguir.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="3a7c8-126">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="3a7c8-127">A aritmética de precisão reduzida é aceitável na avaliação do componente y de destino (dest. y).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="3a7c8-128">Uma implementação deve dar suporte a pelo menos oito bits de fração no argumento de energia.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="3a7c8-129">Os produtos de ponto são calculados com vetores normalizados e os limites de fixe são de-128 a 128.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="3a7c8-130">O erro deve corresponder a uma combinação de [LogP-vs](logp---vs.md) e [exp-vs](exp---vs.md) ou não mais que aproximadamente um bit significativo para um componente de cor de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a7c8-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a7c8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a7c8-132">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3a7c8-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




