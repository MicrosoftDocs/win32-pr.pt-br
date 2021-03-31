---
description: Cria uma textura de volume vazia, ajustando os parâmetros de chamada conforme necessário.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Função D3DXCreateVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930599"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="deefb-103">Função D3DXCreateVolumeTexture</span><span class="sxs-lookup"><span data-stu-id="deefb-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="deefb-104">Cria uma textura de volume vazia, ajustando os parâmetros de chamada conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="deefb-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="deefb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deefb-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="deefb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deefb-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="deefb-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="deefb-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do volume.</span><span class="sxs-lookup"><span data-stu-id="deefb-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-110">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deefb-112">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="deefb-112">Width in pixels.</span></span> <span data-ttu-id="deefb-113">Esse valor deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="deefb-113">This value must be nonzero.</span></span> <span data-ttu-id="deefb-114">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="deefb-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="deefb-115">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deefb-117">Altura em pixels.</span><span class="sxs-lookup"><span data-stu-id="deefb-117">Height in pixels.</span></span> <span data-ttu-id="deefb-118">Esse valor deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="deefb-118">This value must be nonzero.</span></span> <span data-ttu-id="deefb-119">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="deefb-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="deefb-120">*Profundidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deefb-122">Profundidade em pixels.</span><span class="sxs-lookup"><span data-stu-id="deefb-122">Depth in pixels.</span></span> <span data-ttu-id="deefb-123">Esse valor deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="deefb-123">This value must be nonzero.</span></span> <span data-ttu-id="deefb-124">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="deefb-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="deefb-125">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deefb-127">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="deefb-127">Number of mip levels requested.</span></span> <span data-ttu-id="deefb-128">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="deefb-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-129">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deefb-131">0 ou D3DUSAGE \_ dinâmico.</span><span class="sxs-lookup"><span data-stu-id="deefb-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="deefb-132">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="deefb-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="deefb-133">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-134">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="deefb-135">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do volume.</span><span class="sxs-lookup"><span data-stu-id="deefb-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="deefb-136">A textura do volume retornado pode ter um formato diferente daquele especificado pelo formato.</span><span class="sxs-lookup"><span data-stu-id="deefb-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="deefb-137">Os aplicativos devem verificar o formato da textura de volume retornada.</span><span class="sxs-lookup"><span data-stu-id="deefb-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-138">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="deefb-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-139">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="deefb-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="deefb-140">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , descrevendo a classe de memória na qual a textura de volume deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="deefb-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-141">*ppVolumeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="deefb-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-142">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="deefb-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="deefb-143">Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , que representa o objeto de textura de volume criado.</span><span class="sxs-lookup"><span data-stu-id="deefb-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deefb-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deefb-144">Return value</span></span>

<span data-ttu-id="deefb-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deefb-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deefb-146">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deefb-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="deefb-147">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="deefb-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="deefb-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="deefb-148">Remarks</span></span>

<span data-ttu-id="deefb-149">Internamente, o D3DXCreateVolumeTexture usa [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) para ajustar os parâmetros de chamada.</span><span class="sxs-lookup"><span data-stu-id="deefb-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="deefb-150">Portanto, as chamadas para D3DXCreateVolumeTexture geralmente terão êxito onde as chamadas para [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) falharão.</span><span class="sxs-lookup"><span data-stu-id="deefb-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="deefb-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deefb-151">Requirements</span></span>



| <span data-ttu-id="deefb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="deefb-152">Requirement</span></span> | <span data-ttu-id="deefb-153">Valor</span><span class="sxs-lookup"><span data-stu-id="deefb-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deefb-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="deefb-154">Header</span></span><br/>  | <dl> <span data-ttu-id="deefb-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="deefb-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="deefb-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deefb-156">Library</span></span><br/> | <dl> <span data-ttu-id="deefb-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deefb-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="deefb-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="deefb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deefb-159">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="deefb-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
