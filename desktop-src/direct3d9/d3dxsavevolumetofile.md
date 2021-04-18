---
description: Salva um volume em um arquivo no disco.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Função D3DXSaveVolumeToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797569"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="71602-103">Função D3DXSaveVolumeToFile</span><span class="sxs-lookup"><span data-stu-id="71602-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="71602-104">Salva um volume em um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="71602-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="71602-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71602-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="71602-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71602-107">*pDestFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71602-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71602-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71602-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71602-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="71602-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="71602-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="71602-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="71602-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="71602-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="71602-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="71602-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="71602-113">*DestFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71602-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71602-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="71602-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="71602-115">[**D3DXIMAGE \_ Fileformate**](./d3dximage-fileformat.md) especificando o formato de arquivo a ser usado ao salvar.</span><span class="sxs-lookup"><span data-stu-id="71602-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="71602-116">Essa função dá suporte ao salvamento em todos os formatos de **\_ FileFormat do D3DXIMAGE** , exceto no pixmap portátil (. ppm) e no adaptador gráfico Targa/Truevision (. tga).</span><span class="sxs-lookup"><span data-stu-id="71602-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="71602-117">*pSrcVolume* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71602-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71602-118">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="71602-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="71602-119">Ponteiro para a interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contém a imagem a ser salva.</span><span class="sxs-lookup"><span data-stu-id="71602-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="71602-120">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71602-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71602-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="71602-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="71602-122">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém uma paleta de 256 cores.</span><span class="sxs-lookup"><span data-stu-id="71602-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="71602-123">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="71602-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71602-124">*pSrcBox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71602-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71602-125">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="71602-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="71602-126">Ponteiro para uma estrutura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="71602-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="71602-127">Especifica a caixa de origem.</span><span class="sxs-lookup"><span data-stu-id="71602-127">Specifies the source box.</span></span> <span data-ttu-id="71602-128">Defina esse parâmetro como **NULL** para especificar o volume inteiro.</span><span class="sxs-lookup"><span data-stu-id="71602-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71602-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71602-129">Return value</span></span>

<span data-ttu-id="71602-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71602-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71602-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71602-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="71602-132">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="71602-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="71602-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="71602-133">Remarks</span></span>

<span data-ttu-id="71602-134">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="71602-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="71602-135">Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveVolumeToFileW.</span><span class="sxs-lookup"><span data-stu-id="71602-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="71602-136">Caso contrário, a chamada de função é resolvida para >D3DXSaveVolumeToFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="71602-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="71602-137">Essa função manipula a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="71602-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="71602-138">Se o volume for não dinâmico (devido a um parâmetro de uso definido como 0 na criação) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ padrão), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) falhará porque o D3DX não pode bloquear volumes não dinâmicos localizados na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71602-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="71602-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71602-139">Requirements</span></span>



| <span data-ttu-id="71602-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="71602-140">Requirement</span></span> | <span data-ttu-id="71602-141">Valor</span><span class="sxs-lookup"><span data-stu-id="71602-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71602-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71602-142">Header</span></span><br/>  | <dl> <span data-ttu-id="71602-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="71602-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="71602-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71602-144">Library</span></span><br/> | <dl> <span data-ttu-id="71602-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71602-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="71602-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="71602-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71602-147">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="71602-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="71602-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="71602-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="71602-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="71602-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="71602-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="71602-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
