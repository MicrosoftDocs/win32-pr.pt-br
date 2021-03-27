---
title: Valor absoluto
description: Pegue o valor absoluto de um operando de origem usado em uma operação aritmética.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293593"
---
# <a name="absolute-value"></a><span data-ttu-id="842cc-103">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="842cc-103">Absolute Value</span></span>

<span data-ttu-id="842cc-104">Pegue o valor absoluto de um operando de origem usado em uma operação aritmética.</span><span class="sxs-lookup"><span data-stu-id="842cc-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="842cc-105">\_ABS</span><span class="sxs-lookup"><span data-stu-id="842cc-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="842cc-106">Esse modificador é usado somente para ponto flutuante de precisão simples e dupla.</span><span class="sxs-lookup"><span data-stu-id="842cc-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="842cc-107">O modificador **\_ ABS** força o sinal dos números no operando de origem positivo, incluindo os valores inf.</span><span class="sxs-lookup"><span data-stu-id="842cc-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="842cc-108">A aplicação de **\_ ABS** em Nan preserva Nan, embora o padrão de bit Nan específico que resulte não esteja definido.</span><span class="sxs-lookup"><span data-stu-id="842cc-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="842cc-109">Quando \_ ABS é combinado com o modificador de [negação](negate.md) , a combinação força o sinal a ser negativo, como se o modificador de **\_ ABS** for aplicado primeiro, em seguida, o **negará**.</span><span class="sxs-lookup"><span data-stu-id="842cc-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="842cc-110">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="842cc-110">Minimum Shader Model</span></span>

<span data-ttu-id="842cc-111">Esse modificador tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="842cc-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="842cc-112">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="842cc-112">Shader Model</span></span>                                              | <span data-ttu-id="842cc-113">Com suporte</span><span class="sxs-lookup"><span data-stu-id="842cc-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="842cc-114">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="842cc-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="842cc-115">sim</span><span class="sxs-lookup"><span data-stu-id="842cc-115">yes</span></span>       |
| [<span data-ttu-id="842cc-116">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="842cc-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="842cc-117">sim</span><span class="sxs-lookup"><span data-stu-id="842cc-117">yes</span></span>       |
| [<span data-ttu-id="842cc-118">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="842cc-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="842cc-119">sim</span><span class="sxs-lookup"><span data-stu-id="842cc-119">yes</span></span>       |
| [<span data-ttu-id="842cc-120">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="842cc-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="842cc-121">não</span><span class="sxs-lookup"><span data-stu-id="842cc-121">no</span></span>        |
| [<span data-ttu-id="842cc-122">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="842cc-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="842cc-123">não</span><span class="sxs-lookup"><span data-stu-id="842cc-123">no</span></span>        |
| [<span data-ttu-id="842cc-124">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="842cc-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="842cc-125">não</span><span class="sxs-lookup"><span data-stu-id="842cc-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="842cc-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="842cc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="842cc-127">Modificadores de instrução</span><span class="sxs-lookup"><span data-stu-id="842cc-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




