---
description: Cria uma textura vazia, ajustando os parâmetros de chamada conforme necessário.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Função D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506482"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="241d2-103">Função D3DXCreateTexture</span><span class="sxs-lookup"><span data-stu-id="241d2-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="241d2-104">Cria uma textura vazia, ajustando os parâmetros de chamada conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="241d2-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="241d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="241d2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="241d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="241d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="241d2-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="241d2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="241d2-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="241d2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-110">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="241d2-112">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="241d2-112">Width in pixels.</span></span> <span data-ttu-id="241d2-113">Se esse valor for 0, será usado um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="241d2-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="241d2-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="241d2-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-115">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="241d2-117">Altura em pixels.</span><span class="sxs-lookup"><span data-stu-id="241d2-117">Height in pixels.</span></span> <span data-ttu-id="241d2-118">Se esse valor for 0, será usado um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="241d2-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="241d2-119">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="241d2-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-120">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="241d2-122">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="241d2-122">Number of mip levels requested.</span></span> <span data-ttu-id="241d2-123">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="241d2-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-124">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="241d2-126">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="241d2-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="241d2-127">Definir esse sinalizador como **D3DUSAGE \_ RENDERTARGET** indica que a superfície deve ser usada como um destino de renderização chamando o método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="241d2-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="241d2-128">Se **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="241d2-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="241d2-129">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="241d2-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="241d2-130">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-131">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="241d2-132">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="241d2-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="241d2-133">A textura retornada pode ser de um formato diferente daquele especificado, se o dispositivo não oferecer suporte ao formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="241d2-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="241d2-134">Os aplicativos devem verificar o formato da textura retornada para ver se ele corresponde ao formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="241d2-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-135">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="241d2-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-136">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="241d2-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="241d2-137">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="241d2-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="241d2-138">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="241d2-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="241d2-139">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="241d2-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="241d2-140">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="241d2-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="241d2-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="241d2-141">Return value</span></span>

<span data-ttu-id="241d2-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="241d2-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="241d2-143">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="241d2-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="241d2-144">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="241d2-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="241d2-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="241d2-145">Remarks</span></span>

<span data-ttu-id="241d2-146">Internamente, o D3DXCreateTexture usa [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para ajustar os parâmetros de chamada.</span><span class="sxs-lookup"><span data-stu-id="241d2-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="241d2-147">Portanto, as chamadas para D3DXCreateTexture geralmente terão êxito onde as chamadas para [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) falharão.</span><span class="sxs-lookup"><span data-stu-id="241d2-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="241d2-148">Se a altura e a largura forem definidas como [D3DX \_ padrão](other-d3dx-constants.md), um valor de 256 será usado para ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="241d2-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="241d2-149">Se a altura ou a largura for definida como D3DX \_ padrão e o outro parâmetro for definido como um valor numérico, a textura será quadrada com a altura e a largura iguais ao valor numérico.</span><span class="sxs-lookup"><span data-stu-id="241d2-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="241d2-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="241d2-150">Requirements</span></span>



| <span data-ttu-id="241d2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="241d2-151">Requirement</span></span> | <span data-ttu-id="241d2-152">Valor</span><span class="sxs-lookup"><span data-stu-id="241d2-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="241d2-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="241d2-153">Header</span></span><br/>  | <dl> <span data-ttu-id="241d2-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="241d2-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="241d2-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="241d2-155">Library</span></span><br/> | <dl> <span data-ttu-id="241d2-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="241d2-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="241d2-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="241d2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241d2-158">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="241d2-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
