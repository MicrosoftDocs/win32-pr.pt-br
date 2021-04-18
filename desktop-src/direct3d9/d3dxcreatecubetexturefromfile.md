---
description: Cria uma textura de cubo a partir de um arquivo.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Função D3DXCreateCubeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788788"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="06ea6-103">Função D3DXCreateCubeTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="06ea6-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="06ea6-104">Cria uma textura de cubo a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="06ea6-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ea6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06ea6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="06ea6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06ea6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ea6-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06ea6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ea6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="06ea6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="06ea6-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="06ea6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="06ea6-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06ea6-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06ea6-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06ea6-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06ea6-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="06ea6-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="06ea6-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="06ea6-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="06ea6-114">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="06ea6-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="06ea6-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="06ea6-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="06ea6-116">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="06ea6-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06ea6-117">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="06ea6-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="06ea6-118">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="06ea6-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ea6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06ea6-119">Return value</span></span>

<span data-ttu-id="06ea6-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06ea6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06ea6-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06ea6-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06ea6-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="06ea6-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ea6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="06ea6-123">Remarks</span></span>

<span data-ttu-id="06ea6-124">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="06ea6-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="06ea6-125">Se o Unicode for definido, a chamada de função será resolvida como **D3DXCreateCubeTextureFromFileW**.</span><span class="sxs-lookup"><span data-stu-id="06ea6-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="06ea6-126">Caso contrário, a chamada de função é resolvida como **D3DXCreateCubeTextureFromFileA** porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="06ea6-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="06ea6-127">A função é equivalente a D3DXCreateCubeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ padrão, D3DX \_ padrão, 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **NULL**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="06ea6-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="06ea6-128">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="06ea6-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="06ea6-129">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="06ea6-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="06ea6-130">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="06ea6-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="06ea6-131">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="06ea6-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="06ea6-132">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="06ea6-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="06ea6-133">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="06ea6-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="06ea6-134">**D3DXCreateCubeTextureFromFile** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="06ea6-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="06ea6-135">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="06ea6-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="06ea6-136">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="06ea6-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="06ea6-137">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="06ea6-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06ea6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06ea6-138">Requirements</span></span>



| <span data-ttu-id="06ea6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="06ea6-139">Requirement</span></span> | <span data-ttu-id="06ea6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="06ea6-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06ea6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06ea6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="06ea6-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ea6-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="06ea6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06ea6-143">Library</span></span><br/> | <dl> <span data-ttu-id="06ea6-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06ea6-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="06ea6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="06ea6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ea6-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="06ea6-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="06ea6-147">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="06ea6-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
