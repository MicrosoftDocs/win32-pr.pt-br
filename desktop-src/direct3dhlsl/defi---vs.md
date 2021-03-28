---
title: defi-vs
description: Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499117"
---
# <a name="defi---vs"></a><span data-ttu-id="b891e-103">defi-vs</span><span class="sxs-lookup"><span data-stu-id="b891e-103">defi - vs</span></span>

<span data-ttu-id="b891e-104">Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b891e-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b891e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b891e-105">Syntax</span></span>



| <span data-ttu-id="b891e-106">defi DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="b891e-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="b891e-107">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b891e-107">dst is the destination register.</span></span>
-   <span data-ttu-id="b891e-108">integerValue \# é um valor inteiro constante.</span><span class="sxs-lookup"><span data-stu-id="b891e-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b891e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b891e-109">Remarks</span></span>



| <span data-ttu-id="b891e-110">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b891e-110">Vertex shader versions</span></span> | <span data-ttu-id="b891e-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="b891e-111">1\_1</span></span> | <span data-ttu-id="b891e-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b891e-112">2\_0</span></span> | <span data-ttu-id="b891e-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b891e-113">2\_x</span></span> | <span data-ttu-id="b891e-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b891e-114">2\_sw</span></span> | <span data-ttu-id="b891e-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b891e-115">3\_0</span></span> | <span data-ttu-id="b891e-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b891e-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b891e-117">defi</span><span class="sxs-lookup"><span data-stu-id="b891e-117">defi</span></span>                   |      | <span data-ttu-id="b891e-118">x</span><span class="sxs-lookup"><span data-stu-id="b891e-118">x</span></span>    | <span data-ttu-id="b891e-119">x</span><span class="sxs-lookup"><span data-stu-id="b891e-119">x</span></span>    | <span data-ttu-id="b891e-120">x</span><span class="sxs-lookup"><span data-stu-id="b891e-120">x</span></span>     | <span data-ttu-id="b891e-121">x</span><span class="sxs-lookup"><span data-stu-id="b891e-121">x</span></span>    | <span data-ttu-id="b891e-122">x</span><span class="sxs-lookup"><span data-stu-id="b891e-122">x</span></span>     |



 

<span data-ttu-id="b891e-123">A instrução defi define uma constante de sombreador inteiro cujo valor é carregado sempre que um sombreador é definido como um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b891e-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="b891e-124">Elas são chamadas de constantes imediatas.</span><span class="sxs-lookup"><span data-stu-id="b891e-124">These are called immediate constants.</span></span> <span data-ttu-id="b891e-125">Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetVertexShaderConstantI.</span><span class="sxs-lookup"><span data-stu-id="b891e-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="b891e-126">Há duas maneiras de definir uma constante de inteiro em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="b891e-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="b891e-127">Use defi para definir o vetor de constante de inteiro diretamente dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="b891e-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="b891e-128">Use os métodos de API para definir uma constante.</span><span class="sxs-lookup"><span data-stu-id="b891e-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="b891e-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) para definir uma constante de inteiro.</span><span class="sxs-lookup"><span data-stu-id="b891e-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b891e-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b891e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b891e-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b891e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="b891e-132">def-vs</span><span class="sxs-lookup"><span data-stu-id="b891e-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="b891e-133">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="b891e-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 