---
description: Função D3DXCreateVolumeTextureFromFile – cria uma textura de volume a partir de um arquivo.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: Função D3DXCreateVolumeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094294"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="b5423-103">Função D3DXCreateVolumeTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="b5423-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="b5423-104">Cria uma textura de volume a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5423-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5423-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5423-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b5423-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5423-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5423-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5423-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5423-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b5423-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b5423-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do volume.</span><span class="sxs-lookup"><span data-stu-id="b5423-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="b5423-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5423-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5423-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5423-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5423-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5423-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="b5423-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b5423-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b5423-114">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b5423-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b5423-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b5423-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b5423-116">*ppVolumeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5423-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5423-117">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b5423-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="b5423-118">Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="b5423-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5423-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b5423-119">Return value</span></span>

<span data-ttu-id="b5423-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5423-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5423-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5423-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5423-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b5423-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5423-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5423-123">Remarks</span></span>

<span data-ttu-id="b5423-124">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="b5423-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b5423-125">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateVolumeTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="b5423-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="b5423-126">Caso contrário, a chamada de função é resolvida como D3DXCreateVolumeTextureFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="b5423-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="b5423-127">A função é equivalente a D3DXCreateVolumeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ padrão, D3DX \_ padrão, D3DX default \_ , D3DX padrão \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **null**, **NULL**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="b5423-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="b5423-128">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="b5423-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="b5423-129">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="b5423-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="b5423-130">As texturas Mipmapped têm automaticamente cada nível preenchido com a textura carregada.</span><span class="sxs-lookup"><span data-stu-id="b5423-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="b5423-131">Ao carregar imagens em texturas Mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="b5423-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="b5423-132">Se isso acontecer, as imagens precisarão ser carregadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="b5423-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="b5423-133">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b5423-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="b5423-134">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="b5423-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="b5423-135">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="b5423-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="b5423-136">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b5423-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5423-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5423-137">Requirements</span></span>



| <span data-ttu-id="b5423-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5423-138">Requirement</span></span> | <span data-ttu-id="b5423-139">Valor</span><span class="sxs-lookup"><span data-stu-id="b5423-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5423-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5423-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b5423-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5423-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b5423-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5423-142">Library</span></span><br/> | <dl> <span data-ttu-id="b5423-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5423-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5423-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b5423-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5423-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="b5423-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="b5423-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="b5423-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="b5423-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="b5423-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="b5423-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="b5423-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="b5423-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="b5423-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="b5423-150">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b5423-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
