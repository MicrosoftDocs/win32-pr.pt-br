---
description: Define um valor de albedo para cada Texel, substituindo valores albedo anteriores.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Método ID3DXPRTEngine:: SetPerTexelAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370974"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a><span data-ttu-id="1b619-103">Método ID3DXPRTEngine:: SetPerTexelAlbedo</span><span class="sxs-lookup"><span data-stu-id="1b619-103">ID3DXPRTEngine::SetPerTexelAlbedo method</span></span>

<span data-ttu-id="1b619-104">Define um valor de albedo para cada Texel, substituindo valores albedo anteriores.</span><span class="sxs-lookup"><span data-stu-id="1b619-104">Sets an albedo value for each texel, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b619-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b619-105">Syntax</span></span>


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="1b619-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b619-107">*pAlbedoTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b619-107">*pAlbedoTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b619-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="1b619-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="1b619-109">Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) no qual armazenar valores de albedo.</span><span class="sxs-lookup"><span data-stu-id="1b619-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object in which to store albedo values.</span></span>

</dd> <dt>

<span data-ttu-id="1b619-110">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b619-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b619-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b619-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b619-112">Número de canais de cores a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="1b619-112">Number of color channels to set.</span></span> <span data-ttu-id="1b619-113">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="1b619-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="1b619-114">*PGH* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b619-114">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b619-115">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="1b619-115">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="1b619-116">Ponteiro opcional para um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="1b619-116">Optional pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object.</span></span> <span data-ttu-id="1b619-117">Se não for fornecido, um objeto auxiliar de medianiz de textura será criado e destruído internamente.</span><span class="sxs-lookup"><span data-stu-id="1b619-117">If not provided, a texture gutter helper object is created and destroyed internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b619-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b619-118">Return value</span></span>

<span data-ttu-id="1b619-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b619-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b619-120">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b619-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1b619-121">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1b619-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLED3DERR\_OUTOFVIDEOMEMORY, D3DERR\_WASSTILLDRAWING, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b619-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b619-122">Requirements</span></span>



| <span data-ttu-id="1b619-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b619-123">Requirement</span></span> | <span data-ttu-id="1b619-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1b619-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b619-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b619-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1b619-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b619-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1b619-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b619-127">Library</span></span><br/> | <dl> <span data-ttu-id="1b619-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b619-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b619-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b619-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b619-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="1b619-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
