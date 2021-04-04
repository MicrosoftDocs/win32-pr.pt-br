---
description: Cria uma textura a partir de um recurso.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: Função D3DXCreateTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837931"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="cc2e6-103">Função D3DXCreateTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="cc2e6-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="cc2e6-104">Cria uma textura a partir de um recurso.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc2e6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="cc2e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc2e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc2e6-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc2e6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2e6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cc2e6-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="cc2e6-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc2e6-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2e6-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc2e6-112">Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="cc2e6-113">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc2e6-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2e6-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc2e6-115">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="cc2e6-116">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cc2e6-117">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="cc2e6-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cc2e6-119">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc2e6-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc2e6-120">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="cc2e6-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="cc2e6-121">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc2e6-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc2e6-122">Return value</span></span>

<span data-ttu-id="cc2e6-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc2e6-124">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc2e6-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc2e6-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc2e6-126">Remarks</span></span>

<span data-ttu-id="cc2e6-127">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="cc2e6-128">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="cc2e6-129">Caso contrário, a chamada de função é resolvida como D3DXCreateTextureFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="cc2e6-130">A função é equivalente a D3DXCreateTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ padrão, D3DX padrão \_ , D3DX padrão \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="cc2e6-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="cc2e6-131">O recurso que está sendo carregado deve ser do tipo \_ bitmap RT ou RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="cc2e6-132">O tipo de recurso RT \_ RCDATA é usado para carregar formatos diferentes de bitmaps (como. tga,. jpg e. DDS).</span><span class="sxs-lookup"><span data-stu-id="cc2e6-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="cc2e6-133">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="cc2e6-134">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="cc2e6-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="cc2e6-135">Observe que um recurso criado com essa função quando chamado de um objeto IDirect3DDevice9 será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="cc2e6-136">Quando esse método é chamado de um objeto IDirect3DDevice9Ex, o recurso será colocado na classe de memória denotada por D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="cc2e6-137">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="cc2e6-138">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cc2e6-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2e6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2e6-139">Requirements</span></span>



| <span data-ttu-id="cc2e6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2e6-140">Requirement</span></span> | <span data-ttu-id="cc2e6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="cc2e6-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2e6-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc2e6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="cc2e6-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc2e6-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cc2e6-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc2e6-144">Library</span></span><br/> | <dl> <span data-ttu-id="cc2e6-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc2e6-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cc2e6-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc2e6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc2e6-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="cc2e6-148">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="cc2e6-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
