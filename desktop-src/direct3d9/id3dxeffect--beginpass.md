---
description: Inicia uma passagem, dentro da técnica ativa.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Método ID3DXEffect:: BeginPass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798239"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="05a1f-103">Método ID3DXEffect:: BeginPass</span><span class="sxs-lookup"><span data-stu-id="05a1f-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="05a1f-104">Inicia uma passagem, dentro da técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="05a1f-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05a1f-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="05a1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a1f-107">*Passar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05a1f-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a1f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05a1f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05a1f-109">Um índice de inteiro baseado em zero na técnica.</span><span class="sxs-lookup"><span data-stu-id="05a1f-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a1f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05a1f-110">Return value</span></span>

<span data-ttu-id="05a1f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05a1f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05a1f-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05a1f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="05a1f-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="05a1f-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a1f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="05a1f-114">Remarks</span></span>

<span data-ttu-id="05a1f-115">Um aplicativo define uma passagem ativa (dentro de uma técnica ativa) no sistema de efeitos chamando **ID3DXEffect:: BeginPass**.</span><span class="sxs-lookup"><span data-stu-id="05a1f-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="05a1f-116">Um aplicativo sinaliza o final da passagem ativa chamando [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="05a1f-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="05a1f-117">**ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** deve ocorrer em um par correspondente, dentro de um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: End**](id3dxeffect--end.md) calls.</span><span class="sxs-lookup"><span data-stu-id="05a1f-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="05a1f-118">Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**Effect:: setx**](id3dxeffect.md) dentro de um par **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) correspondente, o aplicativo deverá chamar [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) para definir a atualização do dispositivo com as alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="05a1f-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="05a1f-119">Se nenhuma alteração de estado ocorrer em um par **ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** correspondente, não será necessário chamar **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="05a1f-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a1f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05a1f-120">Requirements</span></span>



| <span data-ttu-id="05a1f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a1f-121">Requirement</span></span> | <span data-ttu-id="05a1f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05a1f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a1f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05a1f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="05a1f-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a1f-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="05a1f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05a1f-125">Library</span></span><br/> | <dl> <span data-ttu-id="05a1f-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05a1f-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="05a1f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="05a1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a1f-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="05a1f-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
