---
description: Habilita ou desabilita uma faixa no controlador de animação.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Método ID3DXAnimationController:: SetTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012148"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="b895d-103">Método ID3DXAnimationController:: SetTrackEnable</span><span class="sxs-lookup"><span data-stu-id="b895d-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="b895d-104">Habilita ou desabilita uma faixa no controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="b895d-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b895d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b895d-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="b895d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b895d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b895d-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b895d-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b895d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b895d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b895d-109">Identificador da faixa a ser misturada.</span><span class="sxs-lookup"><span data-stu-id="b895d-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="b895d-110">*Habilitar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b895d-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b895d-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b895d-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b895d-112">Habilitar valor.</span><span class="sxs-lookup"><span data-stu-id="b895d-112">Enable value.</span></span> <span data-ttu-id="b895d-113">Defina como **true** para habilitar essa faixa no controlador ou para **false** para impedir que ele seja misturado.</span><span class="sxs-lookup"><span data-stu-id="b895d-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b895d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b895d-114">Return value</span></span>

<span data-ttu-id="b895d-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b895d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b895d-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b895d-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b895d-117">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b895d-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b895d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b895d-118">Remarks</span></span>

<span data-ttu-id="b895d-119">Para misturar uma faixa com outras faixas, o sinalizador de habilitação deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="b895d-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="b895d-120">Por outro lado, definir o sinalizador como **false** impedirá que a faixa seja misturada com outras faixas.</span><span class="sxs-lookup"><span data-stu-id="b895d-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b895d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b895d-121">Requirements</span></span>



| <span data-ttu-id="b895d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b895d-122">Requirement</span></span> | <span data-ttu-id="b895d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b895d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b895d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b895d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b895d-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b895d-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b895d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b895d-126">Library</span></span><br/> | <dl> <span data-ttu-id="b895d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b895d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b895d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b895d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b895d-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b895d-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
