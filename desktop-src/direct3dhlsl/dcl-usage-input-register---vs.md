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
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998383"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="63d73-103">\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="63d73-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="63d73-104">Declare a associação entre um uso de elemento de vértice e um índice de uso para um registro de entrada de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="63d73-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63d73-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="63d73-106">índice de uso de uso de DCL \_ \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="63d73-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="63d73-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="63d73-107">Where:</span></span>

-   <span data-ttu-id="63d73-108">\_o uso de DCL identifica como os dados de registro serão usados.</span><span class="sxs-lookup"><span data-stu-id="63d73-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="63d73-109">Esse é o mesmo valor que os membros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sem o prefixo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="63d73-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="63d73-110">\_o índice de uso é um índice de inteiro opcional entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="63d73-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="63d73-111">Ele modifica os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="63d73-111">It modifies the usage data.</span></span> <span data-ttu-id="63d73-112">O índice corresponde ao índice de uso em uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="63d73-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="63d73-113">Consulte [declaração de vértice (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="63d73-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="63d73-114">O índice é anexado ao valor de uso (uso de DCL \_ ) sem espaço.</span><span class="sxs-lookup"><span data-stu-id="63d73-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="63d73-115">Se não for fornecido, será considerado 0.</span><span class="sxs-lookup"><span data-stu-id="63d73-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="63d73-116">v \# é um [registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="63d73-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63d73-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="63d73-117">Remarks</span></span>



| <span data-ttu-id="63d73-118">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="63d73-118">Vertex shader versions</span></span> | <span data-ttu-id="63d73-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="63d73-119">1\_1</span></span> | <span data-ttu-id="63d73-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63d73-120">2\_0</span></span> | <span data-ttu-id="63d73-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63d73-121">2\_x</span></span> | <span data-ttu-id="63d73-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63d73-122">2\_sw</span></span> | <span data-ttu-id="63d73-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63d73-123">3\_0</span></span> | <span data-ttu-id="63d73-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63d73-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="63d73-125">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="63d73-125">dcl\_usage</span></span>             | <span data-ttu-id="63d73-126">x</span><span class="sxs-lookup"><span data-stu-id="63d73-126">x</span></span>    | <span data-ttu-id="63d73-127">x</span><span class="sxs-lookup"><span data-stu-id="63d73-127">x</span></span>    | <span data-ttu-id="63d73-128">x</span><span class="sxs-lookup"><span data-stu-id="63d73-128">x</span></span>    | <span data-ttu-id="63d73-129">x</span><span class="sxs-lookup"><span data-stu-id="63d73-129">x</span></span>     | <span data-ttu-id="63d73-130">x</span><span class="sxs-lookup"><span data-stu-id="63d73-130">x</span></span>    | <span data-ttu-id="63d73-131">x</span><span class="sxs-lookup"><span data-stu-id="63d73-131">x</span></span>     |



 

<span data-ttu-id="63d73-132">Todas as \_ instruções de uso de DCL devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="63d73-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63d73-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63d73-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d73-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="63d73-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
