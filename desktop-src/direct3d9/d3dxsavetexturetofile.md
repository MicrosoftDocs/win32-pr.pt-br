---
description: Salva uma textura em um arquivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Função D3DXSaveTextureToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763882"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="a4a27-103">Função D3DXSaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="a4a27-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="a4a27-104">Salva uma textura em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a4a27-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a27-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="a4a27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4a27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a27-107">*pDestFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a27-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a27-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4a27-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4a27-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="a4a27-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="a4a27-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a4a27-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a4a27-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a4a27-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="a4a27-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a4a27-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a4a27-113">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a27-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a27-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a4a27-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="a4a27-115">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="a4a27-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="a4a27-116">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="a4a27-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="a4a27-117">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a27-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a27-118">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="a4a27-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="a4a27-119">Ponteiro para a interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , que contém a textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="a4a27-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="a4a27-120">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a27-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a27-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a4a27-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a4a27-122">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="a4a27-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="a4a27-123">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a4a27-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a27-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4a27-124">Return value</span></span>

<span data-ttu-id="a4a27-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4a27-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4a27-126">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4a27-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a4a27-127">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="a4a27-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a27-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4a27-128">Remarks</span></span>

<span data-ttu-id="a4a27-129">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="a4a27-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="a4a27-130">Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveTextureToFileW.</span><span class="sxs-lookup"><span data-stu-id="a4a27-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="a4a27-131">Caso contrário, a chamada de função é resolvida como D3DXSaveTextureToFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="a4a27-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="a4a27-132">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="a4a27-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="a4a27-133">Se o volume for não dinâmico (devido a um parâmetro de uso definido como 0 na criação) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ padrão), **D3DXSaveTextureToFile** falhará porque o D3DX não pode bloquear volumes não dinâmicos localizados na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a4a27-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a27-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a27-134">Requirements</span></span>



| <span data-ttu-id="a4a27-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a27-135">Requirement</span></span> | <span data-ttu-id="a4a27-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a27-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a27-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4a27-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a4a27-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a27-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a4a27-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4a27-139">Library</span></span><br/> | <dl> <span data-ttu-id="a4a27-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4a27-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a4a27-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4a27-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a27-142">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a4a27-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="a4a27-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="a4a27-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="a4a27-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="a4a27-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
