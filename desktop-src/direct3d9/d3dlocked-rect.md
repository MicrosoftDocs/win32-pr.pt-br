---
description: Descreve uma região retangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Estrutura de D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506495"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="f2943-103">\_Estrutura D3DLOCKED Rect</span><span class="sxs-lookup"><span data-stu-id="f2943-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="f2943-104">Descreve uma região retangular bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f2943-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2943-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2943-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="f2943-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f2943-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2943-107">**Zumbi**</span><span class="sxs-lookup"><span data-stu-id="f2943-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="f2943-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2943-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2943-109">Número de bytes em uma linha da superfície.</span><span class="sxs-lookup"><span data-stu-id="f2943-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="f2943-110">**pBits**</span><span class="sxs-lookup"><span data-stu-id="f2943-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="f2943-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="f2943-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="f2943-112">Ponteiro para os bits bloqueados.</span><span class="sxs-lookup"><span data-stu-id="f2943-112">Pointer to the locked bits.</span></span> <span data-ttu-id="f2943-113">Se um [**Rect**](/previous-versions//dd162897(v=vs.85)) foi fornecido para a chamada [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits será adequadamente deslocado do início da superfície.</span><span class="sxs-lookup"><span data-stu-id="f2943-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2943-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2943-114">Remarks</span></span>

<span data-ttu-id="f2943-115">O Tom dos formatos DXTn é diferente do que foi retornado no DirectX 7.</span><span class="sxs-lookup"><span data-stu-id="f2943-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="f2943-116">Agora, ele se refere ao número de bytes em uma linha de blocos.</span><span class="sxs-lookup"><span data-stu-id="f2943-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="f2943-117">Por exemplo, se você tiver uma largura de 16, terá um timbre de 4 blocos (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="f2943-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="f2943-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2943-118">Requirements</span></span>



| <span data-ttu-id="f2943-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2943-119">Requirement</span></span> | <span data-ttu-id="f2943-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f2943-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2943-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2943-121">Header</span></span><br/> | <dl> <span data-ttu-id="f2943-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2943-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2943-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2943-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2943-124">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f2943-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f2943-125">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="f2943-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="f2943-126">**IDirect3DSurface9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="f2943-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="f2943-127">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="f2943-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
