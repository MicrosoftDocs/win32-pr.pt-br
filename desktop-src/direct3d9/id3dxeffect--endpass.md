---
description: Encerrar uma passagem ativa.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Método ID3DXEffect:: endpass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298651"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="f4217-103">Método ID3DXEffect:: endpass</span><span class="sxs-lookup"><span data-stu-id="f4217-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="f4217-104">Encerrar uma passagem ativa.</span><span class="sxs-lookup"><span data-stu-id="f4217-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4217-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4217-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="f4217-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4217-106">Parameters</span></span>

<span data-ttu-id="f4217-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f4217-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4217-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4217-108">Return value</span></span>

<span data-ttu-id="f4217-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4217-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4217-110">Esse método sempre retorna o valor S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4217-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4217-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4217-111">Remarks</span></span>

<span data-ttu-id="f4217-112">Um aplicativo sinaliza o fim de renderizar uma passagem ativa chamando **ID3DXEffect:: endpass**.</span><span class="sxs-lookup"><span data-stu-id="f4217-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="f4217-113">Cada **ID3DXEffect:: endpass** deve fazer parte de um par correspondente de chamadas [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: endpass** .</span><span class="sxs-lookup"><span data-stu-id="f4217-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="f4217-114">Cada par correspondente de chamadas [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: endpass** deve estar localizado em um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: End**](id3dxeffect--end.md) calls.</span><span class="sxs-lookup"><span data-stu-id="f4217-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="f4217-115">Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**Effect:: setx**](id3dxeffect.md) dentro de um par [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: endpass** correspondente, o aplicativo deverá chamar [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) antes de qualquer chamada DrawxPrimitive para propagar as alterações de estado para o dispositivo antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="f4217-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4217-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4217-116">Requirements</span></span>



| <span data-ttu-id="f4217-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4217-117">Requirement</span></span> | <span data-ttu-id="f4217-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f4217-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4217-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4217-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f4217-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4217-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f4217-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4217-121">Library</span></span><br/> | <dl> <span data-ttu-id="f4217-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4217-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f4217-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4217-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4217-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f4217-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




