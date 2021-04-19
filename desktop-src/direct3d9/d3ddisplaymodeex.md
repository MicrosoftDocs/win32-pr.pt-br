---
description: Informações sobre as propriedades de um modo de exibição.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Estrutura D3DDISPLAYMODEEX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781590"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="5f70d-103">Estrutura D3DDISPLAYMODEEX</span><span class="sxs-lookup"><span data-stu-id="5f70d-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="5f70d-104">Informações sobre as propriedades de um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5f70d-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f70d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f70d-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="5f70d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5f70d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f70d-107">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="5f70d-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-109">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="5f70d-109">The size of this structure.</span></span> <span data-ttu-id="5f70d-110">Isso deve sempre ser definido como sizeof (D3DDISPLAYMODEEX).</span><span class="sxs-lookup"><span data-stu-id="5f70d-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="5f70d-111">**Largura**</span><span class="sxs-lookup"><span data-stu-id="5f70d-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-113">Largura do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5f70d-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="5f70d-114">**Altura**</span><span class="sxs-lookup"><span data-stu-id="5f70d-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-116">Altura do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5f70d-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="5f70d-117">**Taxa_de_atualização**</span><span class="sxs-lookup"><span data-stu-id="5f70d-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-119">Taxa de atualização do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5f70d-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="5f70d-120">**Formato**</span><span class="sxs-lookup"><span data-stu-id="5f70d-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-121">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-122">Formato do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5f70d-122">Format of the display mode.</span></span> <span data-ttu-id="5f70d-123">Consulte [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="5f70d-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f70d-124">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="5f70d-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="5f70d-125">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="5f70d-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f70d-126">Indica se a ordem de varredura é progressiva ou entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="5f70d-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="5f70d-127">Consulte [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="5f70d-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f70d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f70d-128">Remarks</span></span>

<span data-ttu-id="5f70d-129">Essa estrutura é usada em vários métodos para criar e gerenciar dispositivos do Direct3D 9Ex ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) e permuta ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span><span class="sxs-lookup"><span data-stu-id="5f70d-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f70d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f70d-130">Requirements</span></span>



| <span data-ttu-id="5f70d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f70d-131">Requirement</span></span> | <span data-ttu-id="5f70d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5f70d-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f70d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f70d-133">Header</span></span><br/> | <dl> <span data-ttu-id="5f70d-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f70d-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f70d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f70d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f70d-136">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="5f70d-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
