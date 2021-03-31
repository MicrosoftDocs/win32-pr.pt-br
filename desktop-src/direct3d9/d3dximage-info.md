---
description: Retorna uma descrição do conteúdo original de um arquivo de imagem.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Estrutura de D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664001"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="0074c-103">Estrutura de informações do D3DXIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="0074c-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="0074c-104">Retorna uma descrição do conteúdo original de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="0074c-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0074c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0074c-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="0074c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0074c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0074c-107">**Largura**</span><span class="sxs-lookup"><span data-stu-id="0074c-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-109">Largura da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="0074c-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-110">**Altura**</span><span class="sxs-lookup"><span data-stu-id="0074c-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-112">Altura da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="0074c-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-113">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="0074c-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-115">Profundidade da imagem original em pixels.</span><span class="sxs-lookup"><span data-stu-id="0074c-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="0074c-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-118">Número de níveis de MIP na imagem original.</span><span class="sxs-lookup"><span data-stu-id="0074c-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-119">**Formato**</span><span class="sxs-lookup"><span data-stu-id="0074c-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-121">Um valor do tipo enumerado [D3DFORMAT](d3dformat.md) que melhor descreve os dados na imagem original.</span><span class="sxs-lookup"><span data-stu-id="0074c-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0074c-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-123">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-124">Representa o tipo da textura armazenada no arquivo.</span><span class="sxs-lookup"><span data-stu-id="0074c-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="0074c-125">Ele é D3DRTYPE \_ Texture, D3DRTYPE \_ VOLUMETEXTURE ou D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="0074c-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="0074c-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="0074c-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0074c-127">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0074c-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0074c-128">Representa o formato do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="0074c-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0074c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0074c-129">Requirements</span></span>



| <span data-ttu-id="0074c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0074c-130">Requirement</span></span> | <span data-ttu-id="0074c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0074c-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0074c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0074c-132">Header</span></span><br/> | <dl> <span data-ttu-id="0074c-133"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0074c-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0074c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0074c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0074c-135">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="0074c-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
