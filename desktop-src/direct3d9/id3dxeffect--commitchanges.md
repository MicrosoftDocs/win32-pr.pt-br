---
description: Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Método ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173033"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="01479-103">Método ID3DXEffect:: CommitChanges</span><span class="sxs-lookup"><span data-stu-id="01479-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="01479-104">Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="01479-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="01479-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01479-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="01479-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01479-106">Parameters</span></span>

<span data-ttu-id="01479-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="01479-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01479-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01479-108">Return value</span></span>

<span data-ttu-id="01479-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01479-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01479-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01479-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01479-111">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="01479-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="01479-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="01479-112">Remarks</span></span>

<span data-ttu-id="01479-113">Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**ID3DXEffect:: setx**](id3dxeffect.md) dentro de um par [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) correspondente, o aplicativo deverá chamar **ID3DXEffect:: CommitChanges** antes de qualquer chamada DrawxPrimitive para propagar as alterações de estado para o dispositivo antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="01479-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="01479-114">Se nenhuma alteração de estado ocorrer em um par **ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** correspondente, não será necessário chamar **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="01479-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="01479-115">Isso é um pouco diferente para quaisquer parâmetros compartilhados em um efeito clonado.</span><span class="sxs-lookup"><span data-stu-id="01479-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="01479-116">Quando uma técnica está ativa em um efeito clonado (ou seja, quando [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) foi chamado, mas [**ID3DXEffect:: End**](id3dxeffect--end.md) não foi chamado), **ID3DXEffect:: CommitChanges** atualiza os parâmetros que não são compartilhados conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="01479-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="01479-117">Para atualizar um parâmetro compartilhado (somente para um efeito clonado cuja técnica está ativa), chame **ID3DXEffect:: End** para desativar a técnica e **ID3DXEffect:: Begin** para reativar a técnica antes de chamar **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="01479-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="01479-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01479-118">Requirements</span></span>



| <span data-ttu-id="01479-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01479-119">Requirement</span></span> | <span data-ttu-id="01479-120">Valor</span><span class="sxs-lookup"><span data-stu-id="01479-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01479-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01479-121">Header</span></span><br/>  | <dl> <span data-ttu-id="01479-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01479-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="01479-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01479-123">Library</span></span><br/> | <dl> <span data-ttu-id="01479-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01479-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="01479-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="01479-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01479-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="01479-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




