---
title: Estrutura de D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Descreve os parâmetros usados para carregar uma textura de outra textura.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Estrutura D3DX11_TEXTURE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989357"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="725b1-105">\_Estrutura de \_ informações de carregamento de textura D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="725b1-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="725b1-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="725b1-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="725b1-107">Descreve os parâmetros usados para carregar uma textura de outra textura.</span><span class="sxs-lookup"><span data-stu-id="725b1-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="725b1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="725b1-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="725b1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="725b1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="725b1-110">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="725b1-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-111">Tipo: **[ **\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="725b1-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="725b1-112">Caixa de textura de origem (consulte a [**\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="725b1-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="725b1-113">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="725b1-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-114">Tipo: **[ **\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="725b1-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="725b1-115">Caixa textura de destino (consulte a [**\_ caixa D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="725b1-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="725b1-116">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="725b1-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-118">Nível de mipmap de textura de origem, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="725b1-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-119">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="725b1-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-121">Nível de mipmap de textura de destino, consulte [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="725b1-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-122">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="725b1-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-124">Número de níveis de mipmap na textura de origem.</span><span class="sxs-lookup"><span data-stu-id="725b1-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-125">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="725b1-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-127">Primeiro elemento da textura de origem.</span><span class="sxs-lookup"><span data-stu-id="725b1-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-128">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="725b1-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-130">Primeiro elemento da textura de destino.</span><span class="sxs-lookup"><span data-stu-id="725b1-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="725b1-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-133">Número de elementos a serem carregados.</span><span class="sxs-lookup"><span data-stu-id="725b1-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="725b1-134">**Filter**</span><span class="sxs-lookup"><span data-stu-id="725b1-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-135">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-136">Opções de filtragem durante a reamostragem (consulte [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="725b1-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="725b1-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="725b1-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="725b1-138">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="725b1-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="725b1-139">Opções de filtragem ao gerar níveis MIP (consulte o [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="725b1-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="725b1-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="725b1-140">Remarks</span></span>

<span data-ttu-id="725b1-141">Essa estrutura é usada em uma chamada para [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="725b1-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="725b1-142">Os valores padrão são:</span><span class="sxs-lookup"><span data-stu-id="725b1-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="725b1-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="725b1-143">Requirements</span></span>



| <span data-ttu-id="725b1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="725b1-144">Requirement</span></span> | <span data-ttu-id="725b1-145">Valor</span><span class="sxs-lookup"><span data-stu-id="725b1-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="725b1-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="725b1-146">Header</span></span><br/> | <dl> <span data-ttu-id="725b1-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="725b1-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725b1-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="725b1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725b1-149">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="725b1-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

