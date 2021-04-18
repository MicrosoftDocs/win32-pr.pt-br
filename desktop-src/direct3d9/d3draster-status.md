---
description: Descreve o status de rasterização.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Estrutura de D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796143"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="e03df-103">Estrutura de status do D3DRASTER \_</span><span class="sxs-lookup"><span data-stu-id="e03df-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="e03df-104">Descreve o status de rasterização.</span><span class="sxs-lookup"><span data-stu-id="e03df-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e03df-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="e03df-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e03df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e03df-107">**InVBlank**</span><span class="sxs-lookup"><span data-stu-id="e03df-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="e03df-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e03df-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e03df-109">**True** se a rasterização estiver no período vertical em branco.</span><span class="sxs-lookup"><span data-stu-id="e03df-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="e03df-110">**False** se a rasterização não estiver no período vertical em branco.</span><span class="sxs-lookup"><span data-stu-id="e03df-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="e03df-111">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="e03df-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="e03df-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e03df-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e03df-113">Se InVBlank for **false**, esse valor será um inteiro aproximadamente correspondente à linha de exame atual pintada pela rasterização.</span><span class="sxs-lookup"><span data-stu-id="e03df-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="e03df-114">As linhas de verificação são numeradas da mesma maneira que as coordenadas da superfície do Direct3D: 0 é a parte superior da superfície primária, estendendo para o valor (altura da superfície-1) na parte inferior da exibição.</span><span class="sxs-lookup"><span data-stu-id="e03df-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="e03df-115">Se InVBlank for **true**, esse valor será definido como zero e poderá ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="e03df-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e03df-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e03df-116">Requirements</span></span>



| <span data-ttu-id="e03df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e03df-117">Requirement</span></span> | <span data-ttu-id="e03df-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e03df-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e03df-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e03df-119">Header</span></span><br/> | <dl> <span data-ttu-id="e03df-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e03df-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03df-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e03df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03df-122">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e03df-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e03df-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="e03df-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
