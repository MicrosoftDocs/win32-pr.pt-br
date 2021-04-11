---
description: Descreve uma caixa bloqueada (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Estrutura de D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173056"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="900eb-103">Estrutura da caixa de D3DLOCKED \_</span><span class="sxs-lookup"><span data-stu-id="900eb-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="900eb-104">Descreve uma caixa bloqueada (volume).</span><span class="sxs-lookup"><span data-stu-id="900eb-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="900eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="900eb-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="900eb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="900eb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="900eb-107">**De semidensidade**</span><span class="sxs-lookup"><span data-stu-id="900eb-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="900eb-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="900eb-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="900eb-109">Deslocamento de byte da borda esquerda de uma linha para a borda esquerda da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="900eb-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="900eb-110">**SlicePitch**</span><span class="sxs-lookup"><span data-stu-id="900eb-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="900eb-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="900eb-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="900eb-112">Deslocamento de byte do canto superior esquerdo de uma fatia para a parte superior esquerda da próxima fatia mais profunda.</span><span class="sxs-lookup"><span data-stu-id="900eb-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="900eb-113">**pBits**</span><span class="sxs-lookup"><span data-stu-id="900eb-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="900eb-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="900eb-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="900eb-115">Ponteiro para o início da caixa volume.</span><span class="sxs-lookup"><span data-stu-id="900eb-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="900eb-116">Se um [**D3DBOX**](d3dbox.md) foi fornecido para a chamada de Lockbox, o pBits será adequadamente deslocado do início do volume.</span><span class="sxs-lookup"><span data-stu-id="900eb-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="900eb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="900eb-117">Remarks</span></span>

<span data-ttu-id="900eb-118">Os volumes podem ser visualizados como organizados em fatias de largura x altura 2D superfícies empilhadas para fazer um volume de profundidade x altura x de largura.</span><span class="sxs-lookup"><span data-stu-id="900eb-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="900eb-119">Para obter mais informações, consulte [recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="900eb-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="900eb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="900eb-120">Requirements</span></span>



| <span data-ttu-id="900eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="900eb-121">Requirement</span></span> | <span data-ttu-id="900eb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="900eb-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="900eb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="900eb-123">Header</span></span><br/> | <dl> <span data-ttu-id="900eb-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="900eb-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900eb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="900eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900eb-126">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="900eb-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="900eb-127">**IDirect3DVolume9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="900eb-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="900eb-128">**IDirect3DVolumeTexture9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="900eb-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
