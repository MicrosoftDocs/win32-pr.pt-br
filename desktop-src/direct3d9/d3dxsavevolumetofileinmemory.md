---
description: Salva um volume em um buffer. O método cria um buffer ID3DXBuffer para armazenar os dados e retorna esse objeto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Função D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172985"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="736ef-104">Função D3DXSaveVolumeToFileInMemory</span><span class="sxs-lookup"><span data-stu-id="736ef-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="736ef-105">Salva um volume em um buffer.</span><span class="sxs-lookup"><span data-stu-id="736ef-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="736ef-106">O método cria um buffer [**ID3DXBuffer**](id3dxbuffer.md) para armazenar os dados e retorna esse objeto.</span><span class="sxs-lookup"><span data-stu-id="736ef-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="736ef-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="736ef-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="736ef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="736ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="736ef-109">*ppDestBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="736ef-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="736ef-110">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="736ef-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="736ef-111">Endereço de um ponteiro para um buffer [**ID3DXBuffer**](id3dxbuffer.md) que armazenará a imagem.</span><span class="sxs-lookup"><span data-stu-id="736ef-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="736ef-112">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="736ef-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736ef-113">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="736ef-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="736ef-114">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="736ef-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="736ef-115">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="736ef-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="736ef-116">*pSrcVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="736ef-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736ef-117">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="736ef-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="736ef-118">Ponteiro para a interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contém a imagem a ser salva.</span><span class="sxs-lookup"><span data-stu-id="736ef-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="736ef-119">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="736ef-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736ef-120">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="736ef-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="736ef-121">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="736ef-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="736ef-122">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="736ef-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="736ef-123">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="736ef-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736ef-124">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="736ef-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="736ef-125">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="736ef-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="736ef-126">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="736ef-126">Specifies the source box.</span></span> <span data-ttu-id="736ef-127">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="736ef-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="736ef-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="736ef-128">Return value</span></span>

<span data-ttu-id="736ef-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="736ef-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="736ef-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="736ef-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="736ef-131">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="736ef-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="736ef-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736ef-132">Requirements</span></span>



| <span data-ttu-id="736ef-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="736ef-133">Requirement</span></span> | <span data-ttu-id="736ef-134">Valor</span><span class="sxs-lookup"><span data-stu-id="736ef-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="736ef-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="736ef-135">Header</span></span><br/>  | <dl> <span data-ttu-id="736ef-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="736ef-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="736ef-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="736ef-137">Library</span></span><br/> | <dl> <span data-ttu-id="736ef-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="736ef-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="736ef-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="736ef-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="736ef-140">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="736ef-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="736ef-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="736ef-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
