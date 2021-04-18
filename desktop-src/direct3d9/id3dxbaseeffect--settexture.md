---
description: Define uma textura.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'Método ID3DXBaseEffect:: SetTexture (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780721"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="cae32-103">Método ID3DXBaseEffect:: SetTexture</span><span class="sxs-lookup"><span data-stu-id="cae32-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="cae32-104">Define uma textura.</span><span class="sxs-lookup"><span data-stu-id="cae32-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cae32-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="cae32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cae32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae32-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cae32-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae32-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cae32-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cae32-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="cae32-109">Unique identifier.</span></span> <span data-ttu-id="cae32-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="cae32-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="cae32-111">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cae32-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae32-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="cae32-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="cae32-113">Objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="cae32-113">Texture object.</span></span> <span data-ttu-id="cae32-114">Consulte [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="cae32-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae32-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cae32-115">Return value</span></span>

<span data-ttu-id="cae32-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cae32-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cae32-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cae32-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cae32-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cae32-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae32-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cae32-119">Requirements</span></span>



| <span data-ttu-id="cae32-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae32-120">Requirement</span></span> | <span data-ttu-id="cae32-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cae32-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae32-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cae32-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cae32-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae32-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cae32-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cae32-124">Library</span></span><br/> | <dl> <span data-ttu-id="cae32-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae32-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cae32-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae32-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae32-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="cae32-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cae32-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="cae32-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
