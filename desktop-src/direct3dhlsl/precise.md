---
title: Preciso
description: Desabilitação por instrução de refatoração aritmética.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498940"
---
# <a name="precise"></a><span data-ttu-id="7b107-103">Preciso</span><span class="sxs-lookup"><span data-stu-id="7b107-103">Precise</span></span>

<span data-ttu-id="7b107-104">Desabilitação por instrução de refatoração aritmética.</span><span class="sxs-lookup"><span data-stu-id="7b107-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="7b107-105">Preciso (máscara de componente)</span><span class="sxs-lookup"><span data-stu-id="7b107-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="7b107-106">Este modificador requer o sinalizador de sombreador global "refatoração \_ permitida".</span><span class="sxs-lookup"><span data-stu-id="7b107-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="7b107-107">Quando a refatoração \_ permitida estiver presente, os resultados de componentes individuais de instruções individuais poderão ser forçados a permanecerem precisos ou não podem ser refatoráveis por compiladores ou drivers.</span><span class="sxs-lookup"><span data-stu-id="7b107-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="7b107-108">Se os componentes de uma instrução [**Mad**](mad--sm4---asm-.md) estiverem marcados como **precisos**, o hardware deverá executar uma instrução **Mad** ou o equivalente exato e não poderá dividi-lo em uma multiplicação seguida por um Add.</span><span class="sxs-lookup"><span data-stu-id="7b107-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="7b107-109">Por outro lado, um multiplicado seguido por um Add, onde ou ambos são sinalizados como **precisos**, não podem ser mesclados em um **Mad** de fusível.</span><span class="sxs-lookup"><span data-stu-id="7b107-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="7b107-110">Se a refatoração \_ permitida não tiver sido especificada, o modificador **preciso** não será permitido.</span><span class="sxs-lookup"><span data-stu-id="7b107-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="7b107-111">Isso não é necessário porque tudo é preciso.</span><span class="sxs-lookup"><span data-stu-id="7b107-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="7b107-112">O modificador **preciso** afeta qualquer operação, não apenas aritmética.</span><span class="sxs-lookup"><span data-stu-id="7b107-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="7b107-113">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7b107-113">Minimum Shader Model</span></span>

<span data-ttu-id="7b107-114">Esse modificador tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7b107-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="7b107-115">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7b107-115">Shader Model</span></span>                                              | <span data-ttu-id="7b107-116">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7b107-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7b107-117">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7b107-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7b107-118">sim</span><span class="sxs-lookup"><span data-stu-id="7b107-118">yes</span></span>       |
| [<span data-ttu-id="7b107-119">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7b107-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7b107-120">não</span><span class="sxs-lookup"><span data-stu-id="7b107-120">no</span></span>        |
| [<span data-ttu-id="7b107-121">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7b107-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7b107-122">sim</span><span class="sxs-lookup"><span data-stu-id="7b107-122">yes</span></span>       |
| [<span data-ttu-id="7b107-123">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b107-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7b107-124">não</span><span class="sxs-lookup"><span data-stu-id="7b107-124">no</span></span>        |
| [<span data-ttu-id="7b107-125">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b107-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7b107-126">não</span><span class="sxs-lookup"><span data-stu-id="7b107-126">no</span></span>        |
| [<span data-ttu-id="7b107-127">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b107-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7b107-128">não</span><span class="sxs-lookup"><span data-stu-id="7b107-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7b107-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b107-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b107-130">Modificadores de instrução do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="7b107-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




