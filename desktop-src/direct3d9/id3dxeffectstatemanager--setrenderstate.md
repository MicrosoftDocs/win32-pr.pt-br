---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'Método ID3DXEffectStateManager:: setrenderingstate (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815507"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="55c62-103">Método ID3DXEffectStateManager:: setrenderingstate</span><span class="sxs-lookup"><span data-stu-id="55c62-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="55c62-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.</span><span class="sxs-lookup"><span data-stu-id="55c62-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55c62-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="55c62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55c62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c62-107">*Estado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55c62-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c62-108">Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="55c62-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="55c62-109">O estado de renderização a ser definido.</span><span class="sxs-lookup"><span data-stu-id="55c62-109">The render state to set.</span></span> [<span data-ttu-id="55c62-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="55c62-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="55c62-111">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="55c62-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c62-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c62-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55c62-113">O valor do estado de renderização.</span><span class="sxs-lookup"><span data-stu-id="55c62-113">The render state value.</span></span> <span data-ttu-id="55c62-114">Consulte [Estados de efeito (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="55c62-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c62-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55c62-115">Return value</span></span>

<span data-ttu-id="55c62-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55c62-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55c62-117">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55c62-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="55c62-118">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="55c62-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="55c62-119">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="55c62-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="55c62-120">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) falhará.</span><span class="sxs-lookup"><span data-stu-id="55c62-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c62-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55c62-121">Requirements</span></span>



| <span data-ttu-id="55c62-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c62-122">Requirement</span></span> | <span data-ttu-id="55c62-123">Valor</span><span class="sxs-lookup"><span data-stu-id="55c62-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c62-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55c62-124">Header</span></span><br/>  | <dl> <span data-ttu-id="55c62-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c62-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="55c62-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55c62-126">Library</span></span><br/> | <dl> <span data-ttu-id="55c62-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55c62-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55c62-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c62-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="55c62-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
