---
description: Cria uma textura de cubo a partir de um arquivo na memória.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Função D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105795464"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="7b4f6-103">Função D3DXCreateCubeTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="7b4f6-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="7b4f6-104">Cria uma textura de cubo a partir de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b4f6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="7b4f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b4f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4f6-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b4f6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7b4f6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7b4f6-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f6-110">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b4f6-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f6-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b4f6-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b4f6-112">Ponteiro para o arquivo na memória a partir da qual criar o cubemap.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="7b4f6-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f6-114">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b4f6-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f6-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b4f6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b4f6-116">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f6-117">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b4f6-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f6-118">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7b4f6-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="7b4f6-119">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4f6-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b4f6-120">Return value</span></span>

<span data-ttu-id="7b4f6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b4f6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b4f6-122">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7b4f6-123">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4f6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b4f6-124">Remarks</span></span>

<span data-ttu-id="7b4f6-125">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7b4f6-126">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7b4f6-127">A função é equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ padrão, D3DX \_ padrão, 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **NULL**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="7b4f6-128">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="7b4f6-129">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="7b4f6-130">Esse método foi projetado para ser usado para carregar arquivos de imagem armazenados como RT \_ RCDATA, que é um recurso definido pelo aplicativo (dados brutos).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="7b4f6-131">Caso contrário, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="7b4f6-132">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="7b4f6-133">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="7b4f6-134">**D3DXCreateCubeTextureFromFileInMemory** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="7b4f6-135">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="7b4f6-136">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="7b4f6-137">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="7b4f6-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4f6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b4f6-138">Requirements</span></span>



| <span data-ttu-id="7b4f6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4f6-139">Requirement</span></span> | <span data-ttu-id="7b4f6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7b4f6-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4f6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b4f6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7b4f6-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4f6-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7b4f6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b4f6-143">Library</span></span><br/> | <dl> <span data-ttu-id="7b4f6-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b4f6-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7b4f6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b4f6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4f6-146">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7b4f6-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
