---
title: Negar
description: Inverte o sinal do valor de um operando de origem usado em uma operação aritmética.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006876"
---
# <a name="negate"></a><span data-ttu-id="4eefe-103">Negar</span><span class="sxs-lookup"><span data-stu-id="4eefe-103">Negate</span></span>

<span data-ttu-id="4eefe-104">Inverte o sinal do valor de um operando de origem usado em uma operação aritmética.</span><span class="sxs-lookup"><span data-stu-id="4eefe-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="4eefe-105">Para ponto flutuante e instruções de precisão simples e dupla, o modificador de negação inverte o sinal dos números no operando de origem, incluindo os valores INF.</span><span class="sxs-lookup"><span data-stu-id="4eefe-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="4eefe-106">A aplicação de **negação** em NaN preserva Nan, embora o padrão de bit Nan específico que resulte não esteja definido.</span><span class="sxs-lookup"><span data-stu-id="4eefe-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="4eefe-107">Para instruções de inteiro, o modificador de **negação** usa o complemento de 2 do número (s) no operando de origem.</span><span class="sxs-lookup"><span data-stu-id="4eefe-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4eefe-108">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4eefe-108">Minimum Shader Model</span></span>

<span data-ttu-id="4eefe-109">Esse modificador tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4eefe-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="4eefe-110">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4eefe-110">Shader Model</span></span>                                              | <span data-ttu-id="4eefe-111">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4eefe-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4eefe-112">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4eefe-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4eefe-113">sim</span><span class="sxs-lookup"><span data-stu-id="4eefe-113">yes</span></span>       |
| [<span data-ttu-id="4eefe-114">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4eefe-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4eefe-115">sim</span><span class="sxs-lookup"><span data-stu-id="4eefe-115">yes</span></span>       |
| [<span data-ttu-id="4eefe-116">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4eefe-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4eefe-117">sim</span><span class="sxs-lookup"><span data-stu-id="4eefe-117">yes</span></span>       |
| [<span data-ttu-id="4eefe-118">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4eefe-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4eefe-119">não</span><span class="sxs-lookup"><span data-stu-id="4eefe-119">no</span></span>        |
| [<span data-ttu-id="4eefe-120">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4eefe-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4eefe-121">não</span><span class="sxs-lookup"><span data-stu-id="4eefe-121">no</span></span>        |
| [<span data-ttu-id="4eefe-122">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4eefe-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4eefe-123">não</span><span class="sxs-lookup"><span data-stu-id="4eefe-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4eefe-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4eefe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eefe-125">Modificadores de instrução</span><span class="sxs-lookup"><span data-stu-id="4eefe-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




