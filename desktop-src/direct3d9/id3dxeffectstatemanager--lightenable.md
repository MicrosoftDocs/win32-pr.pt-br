---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'Método ID3DXEffectStateManager:: Clareable (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173086"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="43e96-103">Método ID3DXEffectStateManager:: clarear</span><span class="sxs-lookup"><span data-stu-id="43e96-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="43e96-104">Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.</span><span class="sxs-lookup"><span data-stu-id="43e96-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e96-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43e96-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="43e96-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43e96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e96-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="43e96-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e96-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43e96-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43e96-109">O índice de base zero da luz.</span><span class="sxs-lookup"><span data-stu-id="43e96-109">The zero-based index of the light.</span></span> <span data-ttu-id="43e96-110">Esse é o mesmo índice em [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="43e96-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="43e96-111">*Habilitar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43e96-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e96-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43e96-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43e96-113">True para habilitar a luz; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="43e96-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e96-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43e96-114">Return value</span></span>

<span data-ttu-id="43e96-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43e96-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43e96-116">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43e96-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="43e96-117">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="43e96-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="43e96-118">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="43e96-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="43e96-119">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: clareable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) falhará.</span><span class="sxs-lookup"><span data-stu-id="43e96-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e96-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e96-120">Requirements</span></span>



| <span data-ttu-id="43e96-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e96-121">Requirement</span></span> | <span data-ttu-id="43e96-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43e96-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e96-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43e96-123">Header</span></span><br/>  | <dl> <span data-ttu-id="43e96-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e96-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="43e96-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43e96-125">Library</span></span><br/> | <dl> <span data-ttu-id="43e96-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43e96-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="43e96-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43e96-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e96-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="43e96-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
