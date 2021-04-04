---
description: Cria uma textura de volume de um arquivo na memória.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: Função D3DXCreateVolumeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664009"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a><span data-ttu-id="c80e8-103">Função D3DXCreateVolumeTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="c80e8-103">D3DXCreateVolumeTextureFromFileInMemory function</span></span>

<span data-ttu-id="c80e8-104">Cria uma textura de volume de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="c80e8-104">Creates a volume texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="c80e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c80e8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c80e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c80e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c80e8-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c80e8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c80e8-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do volume.</span><span class="sxs-lookup"><span data-stu-id="c80e8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c80e8-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c80e8-112">Ponteiro para o arquivo na memória a partir da qual criar a textura de volume.</span><span class="sxs-lookup"><span data-stu-id="c80e8-112">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-113">*SrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-113">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c80e8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c80e8-115">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c80e8-115">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-116">*ppVolumeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-117">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c80e8-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="c80e8-118">Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="c80e8-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c80e8-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c80e8-119">Return value</span></span>

<span data-ttu-id="c80e8-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c80e8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c80e8-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c80e8-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c80e8-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c80e8-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c80e8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c80e8-123">Remarks</span></span>

<span data-ttu-id="c80e8-124">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="c80e8-124">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c80e8-125">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="c80e8-125">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c80e8-126">A função é equivalente a D3DXCreateVolumeTextureFromFileInMemoryEx (pDevice, pSrcFile, SrcData, D3DX \_ padrão, D3DX \_ padrão, D3DX \_ padrão, D3DX padrão \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **null**, **NULL**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="c80e8-126">The function is equivalent to D3DXCreateVolumeTextureFromFileInMemoryEx(pDevice, pSrcFile, SrcData, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="c80e8-127">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c80e8-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="c80e8-128">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="c80e8-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="c80e8-129">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="c80e8-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="c80e8-130">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c80e8-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c80e8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c80e8-131">Requirements</span></span>



| <span data-ttu-id="c80e8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c80e8-132">Requirement</span></span> | <span data-ttu-id="c80e8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c80e8-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c80e8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c80e8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c80e8-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c80e8-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c80e8-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c80e8-136">Library</span></span><br/> | <dl> <span data-ttu-id="c80e8-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c80e8-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c80e8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c80e8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80e8-139">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="c80e8-139">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="c80e8-140">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="c80e8-140">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="c80e8-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="c80e8-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="c80e8-142">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="c80e8-142">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="c80e8-143">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="c80e8-143">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="c80e8-144">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c80e8-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
