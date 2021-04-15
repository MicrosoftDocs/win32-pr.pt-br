---
title: entrada de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Declare a associação entre um uso de elemento de vértice e um índice de uso para um registro de entrada de sombreador de vértice.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454169"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="91029-103">\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="91029-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="91029-104">Declare a associação entre um uso de elemento de vértice e um índice de uso para um registro de entrada de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="91029-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="91029-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91029-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="91029-106">índice de uso de uso de DCL \_ \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="91029-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="91029-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="91029-107">Where:</span></span>

-   <span data-ttu-id="91029-108">\_o uso de DCL identifica como os dados de registro serão usados.</span><span class="sxs-lookup"><span data-stu-id="91029-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="91029-109">Esse é o mesmo valor que os membros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sem o prefixo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="91029-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="91029-110">\_o índice de uso é um índice de inteiro opcional entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="91029-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="91029-111">Ele modifica os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="91029-111">It modifies the usage data.</span></span> <span data-ttu-id="91029-112">O índice corresponde ao índice de uso em uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="91029-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="91029-113">Consulte [declaração de vértice (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="91029-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="91029-114">O índice é anexado ao valor de uso (uso de DCL \_ ) sem espaço.</span><span class="sxs-lookup"><span data-stu-id="91029-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="91029-115">Se não for fornecido, será considerado 0.</span><span class="sxs-lookup"><span data-stu-id="91029-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="91029-116">v \# é um [registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="91029-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91029-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="91029-117">Remarks</span></span>



| <span data-ttu-id="91029-118">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="91029-118">Vertex shader versions</span></span> | <span data-ttu-id="91029-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="91029-119">1\_1</span></span> | <span data-ttu-id="91029-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91029-120">2\_0</span></span> | <span data-ttu-id="91029-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91029-121">2\_x</span></span> | <span data-ttu-id="91029-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91029-122">2\_sw</span></span> | <span data-ttu-id="91029-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91029-123">3\_0</span></span> | <span data-ttu-id="91029-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91029-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="91029-125">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="91029-125">dcl\_usage</span></span>             | <span data-ttu-id="91029-126">x</span><span class="sxs-lookup"><span data-stu-id="91029-126">x</span></span>    | <span data-ttu-id="91029-127">x</span><span class="sxs-lookup"><span data-stu-id="91029-127">x</span></span>    | <span data-ttu-id="91029-128">x</span><span class="sxs-lookup"><span data-stu-id="91029-128">x</span></span>    | <span data-ttu-id="91029-129">x</span><span class="sxs-lookup"><span data-stu-id="91029-129">x</span></span>     | <span data-ttu-id="91029-130">x</span><span class="sxs-lookup"><span data-stu-id="91029-130">x</span></span>    | <span data-ttu-id="91029-131">x</span><span class="sxs-lookup"><span data-stu-id="91029-131">x</span></span>     |



 

<span data-ttu-id="91029-132">Todas as \_ instruções de uso de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="91029-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91029-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91029-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91029-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="91029-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 