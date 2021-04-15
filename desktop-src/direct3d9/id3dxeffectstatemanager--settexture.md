---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma textura.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'Método ID3DXEffectStateManager:: SetTexture (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506501"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="60225-103">Método ID3DXEffectStateManager:: SetTexture</span><span class="sxs-lookup"><span data-stu-id="60225-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="60225-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma textura.</span><span class="sxs-lookup"><span data-stu-id="60225-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="60225-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60225-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="60225-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60225-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="60225-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60225-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60225-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60225-109">O estágio ao qual a textura é atribuída.</span><span class="sxs-lookup"><span data-stu-id="60225-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="60225-110">Este é o valor de índice em [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) ou [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="60225-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="60225-111">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60225-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60225-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="60225-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="60225-113">Um ponteiro para o objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="60225-113">A pointer to the texture object.</span></span> <span data-ttu-id="60225-114">Pode ser qualquer um dos tipos de textura do Direct3D (cubo, volume, etc.).</span><span class="sxs-lookup"><span data-stu-id="60225-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="60225-115">Consulte [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="60225-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60225-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60225-116">Return value</span></span>

<span data-ttu-id="60225-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60225-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60225-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60225-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="60225-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="60225-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="60225-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="60225-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="60225-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) falhará.</span><span class="sxs-lookup"><span data-stu-id="60225-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="60225-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60225-122">Requirements</span></span>



| <span data-ttu-id="60225-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60225-123">Requirement</span></span> | <span data-ttu-id="60225-124">Valor</span><span class="sxs-lookup"><span data-stu-id="60225-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60225-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60225-125">Header</span></span><br/>  | <dl> <span data-ttu-id="60225-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="60225-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="60225-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60225-127">Library</span></span><br/> | <dl> <span data-ttu-id="60225-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60225-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="60225-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="60225-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60225-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="60225-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
