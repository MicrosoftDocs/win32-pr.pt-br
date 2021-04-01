---
description: Define um retângulo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Estrutura D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664022"
---
# <a name="d3drect-structure"></a><span data-ttu-id="1f389-103">Estrutura D3DRECT</span><span class="sxs-lookup"><span data-stu-id="1f389-103">D3DRECT structure</span></span>

<span data-ttu-id="1f389-104">Define um retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f389-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f389-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f389-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="1f389-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1f389-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f389-107">**X1**</span><span class="sxs-lookup"><span data-stu-id="1f389-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="1f389-108">Tipo: **[ **longo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f389-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f389-109">A coordenada X do canto superior esquerdo do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f389-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="1f389-110">**Y1**</span><span class="sxs-lookup"><span data-stu-id="1f389-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="1f389-111">Tipo: **[ **longo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f389-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f389-112">A coordenada y do canto superior esquerdo do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f389-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="1f389-113">**X2**</span><span class="sxs-lookup"><span data-stu-id="1f389-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="1f389-114">Tipo: **[ **longo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f389-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f389-115">A coordenada x do canto inferior direito do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f389-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="1f389-116">**Y2**</span><span class="sxs-lookup"><span data-stu-id="1f389-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="1f389-117">Tipo: **[ **longo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f389-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f389-118">A coordenada y do canto inferior direito do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1f389-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f389-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f389-119">Requirements</span></span>



| <span data-ttu-id="1f389-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f389-120">Requirement</span></span> | <span data-ttu-id="1f389-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1f389-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f389-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f389-122">Header</span></span><br/> | <dl> <span data-ttu-id="1f389-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f389-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f389-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f389-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f389-125">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="1f389-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="1f389-126">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="1f389-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
