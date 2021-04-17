---
description: Salva uma superfície em um arquivo.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: Função D3DXSaveSurfaceToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780323"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="87581-103">Função D3DXSaveSurfaceToFile</span><span class="sxs-lookup"><span data-stu-id="87581-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="87581-104">Salva uma superfície em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="87581-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="87581-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87581-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="87581-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87581-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87581-107">*pDestFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87581-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87581-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87581-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87581-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="87581-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="87581-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="87581-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="87581-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="87581-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="87581-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="87581-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="87581-113">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87581-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87581-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="87581-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="87581-115">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="87581-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="87581-116">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="87581-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="87581-117">*pSrcSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87581-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87581-118">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="87581-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="87581-119">Ponteiro para a interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , que contém a imagem a ser salva.</span><span class="sxs-lookup"><span data-stu-id="87581-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="87581-120">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87581-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87581-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="87581-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="87581-122">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="87581-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="87581-123">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="87581-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87581-124">*pSrcRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87581-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87581-125">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="87581-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="87581-126">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="87581-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="87581-127">Especifica o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="87581-127">Specifies the source rectangle.</span></span> <span data-ttu-id="87581-128">Defina esse parâmetro como **NULL** para especificar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="87581-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87581-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87581-129">Return value</span></span>

<span data-ttu-id="87581-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87581-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87581-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87581-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="87581-132">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="87581-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="87581-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="87581-133">Remarks</span></span>

<span data-ttu-id="87581-134">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="87581-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="87581-135">Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveSurfaceToFileW.</span><span class="sxs-lookup"><span data-stu-id="87581-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="87581-136">Caso contrário, a chamada de função é resolvida como D3DXSaveSurfaceToFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="87581-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="87581-137">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="87581-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="87581-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87581-138">Requirements</span></span>



| <span data-ttu-id="87581-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="87581-139">Requirement</span></span> | <span data-ttu-id="87581-140">Valor</span><span class="sxs-lookup"><span data-stu-id="87581-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87581-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87581-141">Header</span></span><br/>  | <dl> <span data-ttu-id="87581-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="87581-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="87581-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87581-143">Library</span></span><br/> | <dl> <span data-ttu-id="87581-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87581-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="87581-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="87581-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87581-146">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="87581-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="87581-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="87581-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="87581-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="87581-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
