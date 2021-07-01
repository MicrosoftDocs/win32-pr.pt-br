---
title: dcl_usage entrada (sm1, sm2, sm3 – vs asm)
description: Declare a associação entre o uso de um elemento de vértice e um índice de uso para um registro de entrada do sombreador de vértice.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129683"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="bfa5c-103">entrada de \_ uso dcl (sm1, sm2, sm3 – vs asm)</span><span class="sxs-lookup"><span data-stu-id="bfa5c-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="bfa5c-104">Declare a associação entre o uso de um elemento de vértice e um índice de uso para um registro de entrada do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfa5c-105">Syntax</span></span>

<span data-ttu-id="bfa5c-106">dcl \_ usage \[ index \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="bfa5c-106">dcl\_usage\[usage\_index\] v\#</span></span>



 

<span data-ttu-id="bfa5c-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="bfa5c-107">Where:</span></span>

-   <span data-ttu-id="bfa5c-108">O uso de dcl \_ identifica como os dados de registro serão usados.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="bfa5c-109">Esse é o mesmo valor que os membros [**de D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sem o prefixo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="bfa5c-110">índice \_ de uso é um índice inteiro opcional entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="bfa5c-111">Ele modifica os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-111">It modifies the usage data.</span></span> <span data-ttu-id="bfa5c-112">O índice corresponde ao índice de uso em uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="bfa5c-113">Consulte [Declaração de vértice (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="bfa5c-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="bfa5c-114">O índice é anexado ao valor de uso (uso de dcl \_ ) sem espaço.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="bfa5c-115">Se não for fornecido, supõe-se que seja 0.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="bfa5c-116">v \# é um Registro de [Entrada](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="bfa5c-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bfa5c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfa5c-117">Remarks</span></span>



| <span data-ttu-id="bfa5c-118">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="bfa5c-118">Vertex shader versions</span></span> | <span data-ttu-id="bfa5c-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="bfa5c-119">1\_1</span></span> | <span data-ttu-id="bfa5c-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bfa5c-120">2\_0</span></span> | <span data-ttu-id="bfa5c-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-121">2\_x</span></span> | <span data-ttu-id="bfa5c-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bfa5c-122">2\_sw</span></span> | <span data-ttu-id="bfa5c-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bfa5c-123">3\_0</span></span> | <span data-ttu-id="bfa5c-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bfa5c-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bfa5c-125">uso \_ de dcl</span><span class="sxs-lookup"><span data-stu-id="bfa5c-125">dcl\_usage</span></span>             | <span data-ttu-id="bfa5c-126">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-126">x</span></span>    | <span data-ttu-id="bfa5c-127">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-127">x</span></span>    | <span data-ttu-id="bfa5c-128">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-128">x</span></span>    | <span data-ttu-id="bfa5c-129">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-129">x</span></span>     | <span data-ttu-id="bfa5c-130">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-130">x</span></span>    | <span data-ttu-id="bfa5c-131">x</span><span class="sxs-lookup"><span data-stu-id="bfa5c-131">x</span></span>     |



 

<span data-ttu-id="bfa5c-132">Todas as instruções de uso de dcl \_ devem aparecer antes da primeira instrução executável.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfa5c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfa5c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfa5c-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="bfa5c-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
