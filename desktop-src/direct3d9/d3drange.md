---
description: Define um intervalo.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: Estrutura D3DRANGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797608"
---
# <a name="d3drange-structure"></a><span data-ttu-id="f89ea-103">Estrutura D3DRANGE</span><span class="sxs-lookup"><span data-stu-id="f89ea-103">D3DRANGE structure</span></span>

<span data-ttu-id="f89ea-104">Define um intervalo.</span><span class="sxs-lookup"><span data-stu-id="f89ea-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f89ea-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="f89ea-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f89ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f89ea-107">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="f89ea-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="f89ea-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f89ea-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f89ea-109">Deslocamento, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f89ea-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f89ea-110">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="f89ea-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="f89ea-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f89ea-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f89ea-112">Tamanho, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f89ea-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f89ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f89ea-113">Requirements</span></span>



| <span data-ttu-id="f89ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f89ea-114">Requirement</span></span> | <span data-ttu-id="f89ea-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f89ea-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89ea-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f89ea-116">Header</span></span><br/> | <dl> <span data-ttu-id="f89ea-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f89ea-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89ea-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f89ea-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89ea-119">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f89ea-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
