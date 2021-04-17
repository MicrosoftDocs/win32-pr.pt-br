---
description: Contém dados de rampa vermelho, verde e azul.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Estrutura D3DGAMMARAMP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797933"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="8eb1f-103">Estrutura D3DGAMMARAMP</span><span class="sxs-lookup"><span data-stu-id="8eb1f-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="8eb1f-104">Contém dados de rampa vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="8eb1f-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eb1f-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="8eb1f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8eb1f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8eb1f-107">**vermelho**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="8eb1f-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8eb1f-109">Matriz do elemento de palavra 256 que descreve a rampa de gama vermelha.</span><span class="sxs-lookup"><span data-stu-id="8eb1f-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="8eb1f-110">**amarela**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="8eb1f-111">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8eb1f-112">Matriz do elemento de palavra 256 que descreve a rampa de gama verde.</span><span class="sxs-lookup"><span data-stu-id="8eb1f-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="8eb1f-113">**azul**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="8eb1f-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8eb1f-115">Matriz do elemento de palavra 256 que descreve a rampa de gama azul.</span><span class="sxs-lookup"><span data-stu-id="8eb1f-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8eb1f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb1f-116">Requirements</span></span>



| <span data-ttu-id="8eb1f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb1f-117">Requirement</span></span> | <span data-ttu-id="8eb1f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb1f-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb1f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8eb1f-119">Header</span></span><br/> | <dl> <span data-ttu-id="8eb1f-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb1f-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb1f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb1f-122">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8eb1f-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="8eb1f-123">**GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="8eb1f-124">**SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="8eb1f-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
