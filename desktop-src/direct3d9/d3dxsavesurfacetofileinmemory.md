---
description: Salva uma superfície em um arquivo de imagem.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: Função D3DXSaveSurfaceToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760488"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="8232b-103">Função D3DXSaveSurfaceToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="8232b-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="8232b-104">Salva uma superfície em um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="8232b-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8232b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8232b-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="8232b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8232b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8232b-107">*ppDestBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8232b-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8232b-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8232b-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8232b-109">Endereço de um ponteiro para um [**ID3DXBuffer**](id3dxbuffer.md) que armazenará a imagem.</span><span class="sxs-lookup"><span data-stu-id="8232b-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="8232b-110">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8232b-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8232b-111">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="8232b-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="8232b-112">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="8232b-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="8232b-113">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="8232b-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="8232b-114">*pSrcSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8232b-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8232b-115">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="8232b-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="8232b-116">Ponteiro para a interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que contém a imagem a ser salva.</span><span class="sxs-lookup"><span data-stu-id="8232b-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="8232b-117">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8232b-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8232b-118">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8232b-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8232b-119">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="8232b-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="8232b-120">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8232b-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8232b-121">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8232b-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8232b-122">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="8232b-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="8232b-123">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8232b-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8232b-124">Especifica o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="8232b-124">Specifies the source rectangle.</span></span> <span data-ttu-id="8232b-125">Defina esse parâmetro como **NULL** para especificar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="8232b-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8232b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8232b-126">Return value</span></span>

<span data-ttu-id="8232b-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8232b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8232b-128">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8232b-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8232b-129">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8232b-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8232b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="8232b-130">Remarks</span></span>

<span data-ttu-id="8232b-131">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="8232b-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="8232b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8232b-132">Requirements</span></span>



| <span data-ttu-id="8232b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8232b-133">Requirement</span></span> | <span data-ttu-id="8232b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8232b-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8232b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8232b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8232b-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8232b-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8232b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8232b-137">Library</span></span><br/> | <dl> <span data-ttu-id="8232b-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8232b-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8232b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8232b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8232b-140">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8232b-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="8232b-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="8232b-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
