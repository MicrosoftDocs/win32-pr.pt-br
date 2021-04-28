---
description: Estrutura de D3DX10_IMAGE_INFO – retorna uma descrição do conteúdo original de um arquivo de imagem.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Estrutura de D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105474"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="fb9f8-103">Estrutura de informações de \_ imagem D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="fb9f8-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="fb9f8-104">Retorna uma descrição do conteúdo original de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9f8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb9f8-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="fb9f8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fb9f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb9f8-107">**Largura**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-109">Largura da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-110">**Altura**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-112">Altura da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-113">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-115">Profundidade da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-118">Tamanho da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-118">Size of the texture array.</span></span> <span data-ttu-id="fb9f8-119">As *matrizes* serão 1 para uma única imagem.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-122">Número de níveis de mipmap na imagem original.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-125">Propriedades de recurso diversas ( [**consulte \_ \_ \_ sinalizador d3d10 do recurso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="fb9f8-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-126">**Formato**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-127">Tipo: **[ **\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-128">Um valor do tipo enumerado de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que melhor descreve os dados na imagem original.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-130">Tipo: **[ **d3d10 \_ \_ dimensão de recurso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-131">Representa o tipo da textura armazenada no arquivo.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="fb9f8-132">Consulte [**d3d10 \_ Resource \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="fb9f8-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="fb9f8-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="fb9f8-134">Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="fb9f8-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb9f8-135">Representa o formato do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="fb9f8-135">Represents the format of the image file.</span></span> <span data-ttu-id="fb9f8-136">Consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="fb9f8-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb9f8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb9f8-137">Requirements</span></span>



| <span data-ttu-id="fb9f8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb9f8-138">Requirement</span></span> | <span data-ttu-id="fb9f8-139">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9f8-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9f8-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb9f8-140">Header</span></span><br/> | <dl> <span data-ttu-id="fb9f8-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9f8-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9f8-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fb9f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9f8-143">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="fb9f8-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
