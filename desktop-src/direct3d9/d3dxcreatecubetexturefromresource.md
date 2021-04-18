---
description: Cria uma textura de cubo a partir de um recurso.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: Função D3DXCreateCubeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766551"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="41237-103">Função D3DXCreateCubeTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="41237-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="41237-104">Cria uma textura de cubo a partir de um recurso.</span><span class="sxs-lookup"><span data-stu-id="41237-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="41237-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41237-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="41237-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41237-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41237-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41237-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="41237-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="41237-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="41237-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="41237-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41237-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41237-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41237-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41237-112">Manipule para o módulo em que o recurso está localizado, ou **NULL** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="41237-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="41237-113">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41237-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41237-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41237-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41237-115">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="41237-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="41237-116">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="41237-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="41237-117">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="41237-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="41237-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="41237-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="41237-119">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="41237-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41237-120">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="41237-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="41237-121">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="41237-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41237-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41237-122">Return value</span></span>

<span data-ttu-id="41237-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41237-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41237-124">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41237-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="41237-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="41237-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="41237-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="41237-126">Remarks</span></span>

<span data-ttu-id="41237-127">A configuração do compilador determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="41237-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="41237-128">Se o Unicode for definido, a chamada de função será resolvida como **D3DXCreateCubeTextureFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="41237-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="41237-129">Caso contrário, a chamada de função é resolvida como **D3DXCreateCubeTextureFromResourceA** porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="41237-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="41237-130">A função é equivalente a D3DXCreateCubeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ padrão, D3DX \_ padrão, 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **NULL**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="41237-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="41237-131">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="41237-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="41237-132">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="41237-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="41237-133">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="41237-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="41237-134">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="41237-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="41237-135">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="41237-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="41237-136">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="41237-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="41237-137">**D3DXCreateCubeTextureFromResource** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="41237-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="41237-138">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="41237-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="41237-139">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="41237-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="41237-140">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="41237-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41237-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41237-141">Requirements</span></span>



| <span data-ttu-id="41237-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="41237-142">Requirement</span></span> | <span data-ttu-id="41237-143">Valor</span><span class="sxs-lookup"><span data-stu-id="41237-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41237-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41237-144">Header</span></span><br/>  | <dl> <span data-ttu-id="41237-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="41237-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="41237-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41237-146">Library</span></span><br/> | <dl> <span data-ttu-id="41237-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41237-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="41237-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="41237-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41237-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="41237-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="41237-150">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="41237-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
