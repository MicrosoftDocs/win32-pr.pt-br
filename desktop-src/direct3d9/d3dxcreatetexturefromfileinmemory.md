---
description: Cria uma textura de um arquivo na memória.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: Função D3DXCreateTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664011"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="c4ef2-103">Função D3DXCreateTextureFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="c4ef2-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="c4ef2-104">Cria uma textura de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ef2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4ef2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c4ef2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4ef2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ef2-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4ef2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ef2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c4ef2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c4ef2-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c4ef2-110">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4ef2-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ef2-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ef2-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ef2-112">Ponteiro para o arquivo na memória a partir da qual criar a textura.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c4ef2-113">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4ef2-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ef2-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ef2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ef2-115">Tamanho em bytes do arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="c4ef2-116">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4ef2-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ef2-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="c4ef2-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="c4ef2-118">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ef2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4ef2-119">Return value</span></span>

<span data-ttu-id="c4ef2-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4ef2-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4ef2-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c4ef2-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ef2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4ef2-123">Remarks</span></span>

<span data-ttu-id="c4ef2-124">A função é equivalente a D3DXCreateTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ padrão, D3DX padrão \_ , D3DX padrão \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="c4ef2-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="c4ef2-125">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c4ef2-126">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="c4ef2-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c4ef2-127">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="c4ef2-128">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="c4ef2-129">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="c4ef2-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="c4ef2-130">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c4ef2-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ef2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ef2-131">Requirements</span></span>



| <span data-ttu-id="c4ef2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ef2-132">Requirement</span></span> | <span data-ttu-id="c4ef2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c4ef2-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ef2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4ef2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ef2-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ef2-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c4ef2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4ef2-136">Library</span></span><br/> | <dl> <span data-ttu-id="c4ef2-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ef2-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c4ef2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4ef2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ef2-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="c4ef2-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="c4ef2-140">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c4ef2-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
