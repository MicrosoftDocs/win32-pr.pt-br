---
description: Define a velocidade da faixa. A velocidade da faixa é semelhante a um multiplicador que é usado para acelerar ou reduzir a reprodução da faixa.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'Método ID3DXAnimationController:: SetTrackSpeed (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298840"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="a9537-104">Método ID3DXAnimationController:: SetTrackSpeed</span><span class="sxs-lookup"><span data-stu-id="a9537-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="a9537-105">Define a velocidade da faixa.</span><span class="sxs-lookup"><span data-stu-id="a9537-105">Sets the track speed.</span></span> <span data-ttu-id="a9537-106">A velocidade da faixa é semelhante a um multiplicador que é usado para acelerar ou reduzir a reprodução da faixa.</span><span class="sxs-lookup"><span data-stu-id="a9537-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9537-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9537-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="a9537-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9537-109">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9537-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9537-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9537-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9537-111">Identificador da faixa na qual definir a velocidade.</span><span class="sxs-lookup"><span data-stu-id="a9537-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="a9537-112">*Velocidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9537-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9537-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9537-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9537-114">Nova velocidade.</span><span class="sxs-lookup"><span data-stu-id="a9537-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9537-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9537-115">Return value</span></span>

<span data-ttu-id="a9537-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9537-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9537-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9537-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a9537-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a9537-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9537-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9537-119">Requirements</span></span>



| <span data-ttu-id="a9537-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9537-120">Requirement</span></span> | <span data-ttu-id="a9537-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a9537-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9537-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9537-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a9537-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9537-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a9537-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9537-124">Library</span></span><br/> | <dl> <span data-ttu-id="a9537-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9537-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9537-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9537-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9537-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a9537-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
