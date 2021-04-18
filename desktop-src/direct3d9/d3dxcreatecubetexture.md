---
description: Cria uma textura de cubo vazia, ajustando os parâmetros de chamada conforme necessário.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Função D3DXCreateCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793732"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="73ea1-103">Função D3DXCreateCubeTexture</span><span class="sxs-lookup"><span data-stu-id="73ea1-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="73ea1-104">Cria uma textura de cubo vazia, ajustando os parâmetros de chamada conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="73ea1-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ea1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73ea1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="73ea1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ea1-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="73ea1-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="73ea1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-110">*Tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ea1-112">Largura e altura da textura do cubo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="73ea1-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="73ea1-113">Por exemplo, se a textura do cubo for de 8 pixels por cubo de 8 pixels, o valor desse parâmetro deverá ser 8.</span><span class="sxs-lookup"><span data-stu-id="73ea1-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-114">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ea1-116">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="73ea1-116">Number of mip levels requested.</span></span> <span data-ttu-id="73ea1-117">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="73ea1-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-118">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ea1-120">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="73ea1-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="73ea1-121">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="73ea1-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="73ea1-122">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="73ea1-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="73ea1-123">Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="73ea1-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="73ea1-124">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="73ea1-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-125">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-126">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="73ea1-127">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="73ea1-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="73ea1-128">A textura do cubo retornado pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="73ea1-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="73ea1-129">Os aplicativos devem verificar o formato da textura do cubo retornado.</span><span class="sxs-lookup"><span data-stu-id="73ea1-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-130">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-131">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="73ea1-132">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura do cubo deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="73ea1-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="73ea1-133">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="73ea1-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea1-134">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="73ea1-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="73ea1-135">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="73ea1-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ea1-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73ea1-136">Return value</span></span>

<span data-ttu-id="73ea1-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73ea1-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73ea1-138">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73ea1-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="73ea1-139">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="73ea1-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="73ea1-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="73ea1-140">Remarks</span></span>

<span data-ttu-id="73ea1-141">Texturas de cubos diferem de outras superfícies em que são coleções de superfícies.</span><span class="sxs-lookup"><span data-stu-id="73ea1-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="73ea1-142">Internamente, o D3DXCreateCubeTexture usa [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) para ajustar os parâmetros de chamada.</span><span class="sxs-lookup"><span data-stu-id="73ea1-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="73ea1-143">Portanto, as chamadas para D3DXCreateCubeTexture geralmente terão êxito onde as chamadas para [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) falharão.</span><span class="sxs-lookup"><span data-stu-id="73ea1-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ea1-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ea1-144">Requirements</span></span>



| <span data-ttu-id="73ea1-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ea1-145">Requirement</span></span> | <span data-ttu-id="73ea1-146">Valor</span><span class="sxs-lookup"><span data-stu-id="73ea1-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73ea1-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73ea1-147">Header</span></span><br/>  | <dl> <span data-ttu-id="73ea1-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ea1-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="73ea1-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73ea1-149">Library</span></span><br/> | <dl> <span data-ttu-id="73ea1-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ea1-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="73ea1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="73ea1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ea1-152">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="73ea1-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
