---
description: Define um volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Estrutura D3DBOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172951"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="36fa2-103">Estrutura D3DBOX</span><span class="sxs-lookup"><span data-stu-id="36fa2-103">D3DBOX structure</span></span>

<span data-ttu-id="36fa2-104">Define um volume.</span><span class="sxs-lookup"><span data-stu-id="36fa2-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="36fa2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36fa2-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="36fa2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="36fa2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36fa2-107">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="36fa2-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-109">Posição do lado esquerdo da caixa no eixo x.</span><span class="sxs-lookup"><span data-stu-id="36fa2-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="36fa2-110">**Top**</span><span class="sxs-lookup"><span data-stu-id="36fa2-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-112">Posição da parte superior da caixa no eixo y.</span><span class="sxs-lookup"><span data-stu-id="36fa2-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="36fa2-113">**Certo**</span><span class="sxs-lookup"><span data-stu-id="36fa2-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-115">Posição do lado direito da caixa no eixo x.</span><span class="sxs-lookup"><span data-stu-id="36fa2-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="36fa2-116">**Inferior**</span><span class="sxs-lookup"><span data-stu-id="36fa2-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-118">Posição da parte inferior da caixa no eixo y.</span><span class="sxs-lookup"><span data-stu-id="36fa2-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="36fa2-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="36fa2-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-121">Posição da frente da caixa no eixo z.</span><span class="sxs-lookup"><span data-stu-id="36fa2-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="36fa2-122">**Voltar**</span><span class="sxs-lookup"><span data-stu-id="36fa2-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="36fa2-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36fa2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="36fa2-124">Posição da parte de trás da caixa no eixo z.</span><span class="sxs-lookup"><span data-stu-id="36fa2-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36fa2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="36fa2-125">Remarks</span></span>

<span data-ttu-id="36fa2-126">**D3DBOX** inclui as bordas esquerda, superior e frontal; no entanto, as bordas direita, inferior e traseira não são incluídas.</span><span class="sxs-lookup"><span data-stu-id="36fa2-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="36fa2-127">Por exemplo, uma caixa com 100 unidades de largura e começa em 0 (portanto, a inclusão de pontos até e incluindo 99) seria expressa com um valor de 0 para o membro esquerdo e um valor de 100 para o membro correto.</span><span class="sxs-lookup"><span data-stu-id="36fa2-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="36fa2-128">Observe que um valor de 99 não é usado para o membro correto.</span><span class="sxs-lookup"><span data-stu-id="36fa2-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="36fa2-129">As restrições de ordenação do lado observado para **D3DBOX** são da esquerda para a direita, de cima para baixo e de frente para trás.</span><span class="sxs-lookup"><span data-stu-id="36fa2-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fa2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36fa2-130">Requirements</span></span>



| <span data-ttu-id="36fa2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="36fa2-131">Requirement</span></span> | <span data-ttu-id="36fa2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="36fa2-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36fa2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36fa2-133">Header</span></span><br/> | <dl> <span data-ttu-id="36fa2-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36fa2-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36fa2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="36fa2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fa2-136">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="36fa2-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
