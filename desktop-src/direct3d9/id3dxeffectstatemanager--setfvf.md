---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'Método ID3DXEffectStateManager:: SetFVF (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763495"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="5b1f0-103">Método ID3DXEffectStateManager:: SetFVF</span><span class="sxs-lookup"><span data-stu-id="5b1f0-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="5b1f0-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.</span><span class="sxs-lookup"><span data-stu-id="5b1f0-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b1f0-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="5b1f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b1f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1f0-107">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b1f0-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1f0-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b1f0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b1f0-109">A constante FVF, que determina como interpretar os dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="5b1f0-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="5b1f0-110">Consulte [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="5b1f0-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1f0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b1f0-111">Return value</span></span>

<span data-ttu-id="5b1f0-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b1f0-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b1f0-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b1f0-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5b1f0-114">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="5b1f0-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5b1f0-115">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="5b1f0-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5b1f0-116">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) falhará.</span><span class="sxs-lookup"><span data-stu-id="5b1f0-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1f0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b1f0-117">Requirements</span></span>



| <span data-ttu-id="5b1f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b1f0-118">Requirement</span></span> | <span data-ttu-id="5b1f0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5b1f0-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1f0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b1f0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5b1f0-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b1f0-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5b1f0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b1f0-122">Library</span></span><br/> | <dl> <span data-ttu-id="5b1f0-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b1f0-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5b1f0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b1f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1f0-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5b1f0-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
