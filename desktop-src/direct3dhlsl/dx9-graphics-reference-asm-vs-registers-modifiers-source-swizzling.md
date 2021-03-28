---
title: Swizzling de registro de origem (referência de HLSL VS)
description: Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário. Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365313"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="b17e4-105">Swizzling de registro de origem (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="b17e4-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="b17e4-106">Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="b17e4-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="b17e4-107">Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário.</span><span class="sxs-lookup"><span data-stu-id="b17e4-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="b17e4-108">Swizzling não afeta os dados de registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b17e4-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="b17e4-109">Swizzling de componente</span><span class="sxs-lookup"><span data-stu-id="b17e4-109">Component Swizzling</span></span>

<span data-ttu-id="b17e4-110">Conforme mostrado na tabela a seguir, swizzling pode ser aplicado aos componentes individuais dos dados de registro de origem (onde é um dos registradores de entrada válidos do sombreador de vértice [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span><span class="sxs-lookup"><span data-stu-id="b17e4-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="b17e4-111">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="b17e4-111">Component modifier</span></span>                 | <span data-ttu-id="b17e4-112">Description</span><span class="sxs-lookup"><span data-stu-id="b17e4-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="b17e4-113">r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\]</span><span class="sxs-lookup"><span data-stu-id="b17e4-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="b17e4-114">Swizzle de origem</span><span class="sxs-lookup"><span data-stu-id="b17e4-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="b17e4-115">Todos os quatro componentes são sempre copiados.</span><span class="sxs-lookup"><span data-stu-id="b17e4-115">All four components are always copied.</span></span> <span data-ttu-id="b17e4-116">Se menos de quatro componentes forem especificados, o último componente será repetido (XY significa. xyyy).</span><span class="sxs-lookup"><span data-stu-id="b17e4-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="b17e4-117">Se nenhum componente for especificado, x será repetido (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="b17e4-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="b17e4-118">Os componentes podem aparecer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="b17e4-118">The components can appear in any order.</span></span> <span data-ttu-id="b17e4-119">V0. YWX resulta em V0. ywxx.</span><span class="sxs-lookup"><span data-stu-id="b17e4-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="b17e4-120">Os componentes RGBA podem ser usados respectivamente para xyzw (r para x, g para b, etc.).</span><span class="sxs-lookup"><span data-stu-id="b17e4-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="b17e4-121">Essas instruções implementam a origem-registrar um único componente swizzles: exp, expp, log, LogP, pow, RCP, RSQ.</span><span class="sxs-lookup"><span data-stu-id="b17e4-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="b17e4-122">O resultado dessas instruções é copiado para todos os quatro componentes de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b17e4-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="b17e4-123">Swizzling não pode ser usado nas instruções [M3X2-vs](m3x2---vs.md), [m3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)e [m4x4-vs](m4x4---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="b17e4-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b17e4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b17e4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b17e4-125">Modificadores de registro do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b17e4-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




