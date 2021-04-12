---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma amostra.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'Método ID3DXEffectStateManager:: setsamplestate (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298685"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="067d1-103">Método ID3DXEffectStateManager:: setsamplestate</span><span class="sxs-lookup"><span data-stu-id="067d1-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="067d1-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma amostra.</span><span class="sxs-lookup"><span data-stu-id="067d1-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="067d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="067d1-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="067d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="067d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067d1-107">*Amostra* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="067d1-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067d1-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="067d1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="067d1-109">O número de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="067d1-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="067d1-110">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="067d1-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067d1-111">Tipo: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="067d1-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="067d1-112">Identifica o estado de amostra, que pode especificar a filtragem, o endereçamento ou a cor da borda.</span><span class="sxs-lookup"><span data-stu-id="067d1-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="067d1-113">Consulte [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="067d1-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="067d1-114">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="067d1-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067d1-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="067d1-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="067d1-116">Um valor de um dos tipos de estado de amostra no tipo.</span><span class="sxs-lookup"><span data-stu-id="067d1-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067d1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="067d1-117">Return value</span></span>

<span data-ttu-id="067d1-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="067d1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="067d1-119">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="067d1-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="067d1-120">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="067d1-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="067d1-121">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="067d1-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="067d1-122">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) falhará.</span><span class="sxs-lookup"><span data-stu-id="067d1-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="067d1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="067d1-123">Requirements</span></span>



| <span data-ttu-id="067d1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="067d1-124">Requirement</span></span> | <span data-ttu-id="067d1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="067d1-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="067d1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="067d1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="067d1-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="067d1-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="067d1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="067d1-128">Library</span></span><br/> | <dl> <span data-ttu-id="067d1-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="067d1-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="067d1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="067d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067d1-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="067d1-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
