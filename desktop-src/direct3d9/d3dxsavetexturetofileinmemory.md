---
description: Salva uma textura em um arquivo de imagem.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: Função D3DXSaveTextureToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091961"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="268b5-103">Função D3DXSaveTextureToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="268b5-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="268b5-104">Salva uma textura em um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="268b5-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="268b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="268b5-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="268b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="268b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268b5-107">*ppDestBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="268b5-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="268b5-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="268b5-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="268b5-109">Endereço de um ponteiro para um [**ID3DXBuffer**](id3dxbuffer.md) que armazenará a imagem.</span><span class="sxs-lookup"><span data-stu-id="268b5-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="268b5-110">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="268b5-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268b5-111">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="268b5-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="268b5-112">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="268b5-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="268b5-113">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="268b5-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="268b5-114">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="268b5-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268b5-115">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="268b5-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="268b5-116">Ponteiro para a interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que contém a imagem a ser salva.</span><span class="sxs-lookup"><span data-stu-id="268b5-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="268b5-117">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="268b5-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268b5-118">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="268b5-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="268b5-119">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="268b5-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="268b5-120">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="268b5-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268b5-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="268b5-121">Return value</span></span>

<span data-ttu-id="268b5-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="268b5-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="268b5-123">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="268b5-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="268b5-124">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="268b5-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="268b5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="268b5-125">Remarks</span></span>

<span data-ttu-id="268b5-126">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="268b5-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="268b5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="268b5-127">Requirements</span></span>



| <span data-ttu-id="268b5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="268b5-128">Requirement</span></span> | <span data-ttu-id="268b5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="268b5-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="268b5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="268b5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="268b5-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="268b5-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="268b5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="268b5-132">Library</span></span><br/> | <dl> <span data-ttu-id="268b5-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="268b5-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="268b5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="268b5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268b5-135">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="268b5-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="268b5-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="268b5-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="268b5-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="268b5-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
