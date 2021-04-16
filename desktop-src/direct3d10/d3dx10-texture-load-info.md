---
description: Descreve os parâmetros usados para carregar uma textura de outra textura.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Estrutura de D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772741"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="9d3f3-103">\_Estrutura de \_ informações de carregamento de textura D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="9d3f3-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="9d3f3-104">Descreve os parâmetros usados para carregar uma textura de outra textura.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d3f3-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="9d3f3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9d3f3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d3f3-107">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-108">Tipo: **[ **\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="9d3f3-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-109">Caixa de textura de origem (consulte a [**\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-110">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-111">Tipo: **[ **\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="9d3f3-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-112">Caixa textura de destino (consulte a [**\_ caixa d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-113">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-115">Nível de mipmap de textura de origem, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-116">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-118">Nível de mipmap de textura de destino, consulte [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-119">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-121">Número de níveis de mipmap na textura de origem.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-122">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-124">Primeiro elemento da textura de origem.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-125">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-127">Primeiro elemento da textura de destino.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-130">Número de elementos a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-133">Opções de filtragem durante a reamostragem (consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9d3f3-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="9d3f3-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d3f3-136">Opções de filtragem ao gerar níveis MIP (consulte o [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d3f3-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d3f3-137">Remarks</span></span>

<span data-ttu-id="9d3f3-138">Essa estrutura é usada em uma chamada para [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3f3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d3f3-139">Requirements</span></span>



| <span data-ttu-id="9d3f3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d3f3-140">Requirement</span></span> | <span data-ttu-id="9d3f3-141">Valor</span><span class="sxs-lookup"><span data-stu-id="9d3f3-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3f3-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d3f3-142">Header</span></span><br/> | <dl> <span data-ttu-id="9d3f3-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d3f3-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d3f3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d3f3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3f3-145">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="9d3f3-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
