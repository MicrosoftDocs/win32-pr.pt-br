---
title: Estrutura de D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. | Estrutura de D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Estrutura D3DX11_IMAGE_INFO Direct3D 11
- Ponteiro de estrutura LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968693"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="633ba-107">Estrutura de informações de \_ imagem D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="633ba-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="633ba-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="633ba-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="633ba-109">Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas.</span><span class="sxs-lookup"><span data-stu-id="633ba-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="633ba-110">Um valor de D3DX11 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="633ba-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="633ba-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="633ba-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="633ba-112">Membros</span><span class="sxs-lookup"><span data-stu-id="633ba-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="633ba-113">**Largura**</span><span class="sxs-lookup"><span data-stu-id="633ba-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-115">A largura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="633ba-115">The target width of the texture.</span></span> <span data-ttu-id="633ba-116">Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa largura de destino.</span><span class="sxs-lookup"><span data-stu-id="633ba-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-117">**Altura**</span><span class="sxs-lookup"><span data-stu-id="633ba-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-119">A altura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="633ba-119">The target height of the texture.</span></span> <span data-ttu-id="633ba-120">Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.</span><span class="sxs-lookup"><span data-stu-id="633ba-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-121">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="633ba-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-123">A profundidade da textura.</span><span class="sxs-lookup"><span data-stu-id="633ba-123">The depth of the texture.</span></span> <span data-ttu-id="633ba-124">Isso se aplica somente a texturas de volume.</span><span class="sxs-lookup"><span data-stu-id="633ba-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="633ba-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-127">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="633ba-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-128">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="633ba-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-129">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-130">O número máximo de níveis de mipmap na textura.</span><span class="sxs-lookup"><span data-stu-id="633ba-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="633ba-131">Consulte os comentários em [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="633ba-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="633ba-132">Usar 0 ou D3DX11 \_ padrão fará com que uma cadeia de mipmap completa seja criada.</span><span class="sxs-lookup"><span data-stu-id="633ba-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-133">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="633ba-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="633ba-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-135">Diversas propriedades de recurso especificadas com um sinalizador de [**\_ \_ \_ sinalizador variado de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="633ba-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-136">**Formato**</span><span class="sxs-lookup"><span data-stu-id="633ba-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-137">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="633ba-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-138">Uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) especificando o formato em que a textura estará depois de ser carregada.</span><span class="sxs-lookup"><span data-stu-id="633ba-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-139">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="633ba-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-140">Tipo: **[ **D3D11 \_ \_ dimensão de recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="633ba-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-141">Um valor de [**\_ \_ dimensão de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , que identifica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="633ba-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="633ba-142">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="633ba-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="633ba-143">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="633ba-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="633ba-144">Um valor de [**\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md) , que identifica o formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="633ba-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="633ba-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="633ba-145">Remarks</span></span>

<span data-ttu-id="633ba-146">Essa estrutura é usada por métodos como: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="633ba-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="633ba-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="633ba-147">Requirements</span></span>



| <span data-ttu-id="633ba-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="633ba-148">Requirement</span></span> | <span data-ttu-id="633ba-149">Valor</span><span class="sxs-lookup"><span data-stu-id="633ba-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="633ba-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="633ba-150">Header</span></span><br/> | <dl> <span data-ttu-id="633ba-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="633ba-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633ba-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="633ba-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633ba-153">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="633ba-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

