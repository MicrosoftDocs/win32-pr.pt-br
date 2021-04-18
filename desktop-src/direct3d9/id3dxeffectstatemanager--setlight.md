---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'Método ID3DXEffectStateManager:: SetLight (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781178"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="7c03a-103">Método ID3DXEffectStateManager:: SetLight</span><span class="sxs-lookup"><span data-stu-id="7c03a-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="7c03a-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.</span><span class="sxs-lookup"><span data-stu-id="7c03a-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c03a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c03a-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="7c03a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c03a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c03a-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7c03a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c03a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c03a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c03a-109">O índice de base zero da luz.</span><span class="sxs-lookup"><span data-stu-id="7c03a-109">The zero-based index of the light.</span></span> <span data-ttu-id="7c03a-110">Esse é o mesmo índice em [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="7c03a-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="7c03a-111">*plight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c03a-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c03a-112">Tipo: **const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c03a-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="7c03a-113">O objeto Light.</span><span class="sxs-lookup"><span data-stu-id="7c03a-113">The light object.</span></span> <span data-ttu-id="7c03a-114">Consulte [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="7c03a-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c03a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c03a-115">Return value</span></span>

<span data-ttu-id="7c03a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c03a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c03a-117">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c03a-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="7c03a-118">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7c03a-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="7c03a-119">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="7c03a-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="7c03a-120">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) falhará.</span><span class="sxs-lookup"><span data-stu-id="7c03a-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c03a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c03a-121">Requirements</span></span>



| <span data-ttu-id="7c03a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c03a-122">Requirement</span></span> | <span data-ttu-id="7c03a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c03a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c03a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7c03a-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c03a-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7c03a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c03a-126">Library</span></span><br/> | <dl> <span data-ttu-id="7c03a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c03a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c03a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c03a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c03a-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="7c03a-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
