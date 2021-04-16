---
description: Remove todos os eventos de uma faixa de animação especificada.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'Método ID3DXAnimationController:: UnkeyAllTrackEvents (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765338"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="b2b4b-103">Método ID3DXAnimationController:: UnkeyAllTrackEvents</span><span class="sxs-lookup"><span data-stu-id="b2b4b-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="b2b4b-104">Remove todos os eventos de uma faixa de animação especificada.</span><span class="sxs-lookup"><span data-stu-id="b2b4b-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2b4b-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="b2b4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2b4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b4b-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2b4b-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b4b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2b4b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2b4b-109">Identificador do controle no qual todos os eventos devem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="b2b4b-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b4b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2b4b-110">Return value</span></span>

<span data-ttu-id="b2b4b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2b4b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2b4b-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2b4b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b2b4b-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b2b4b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b4b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2b4b-114">Remarks</span></span>

<span data-ttu-id="b2b4b-115">Esse método impede a execução de todos os eventos agendados anteriormente na faixa e descarta todos os dados associados a esses eventos.</span><span class="sxs-lookup"><span data-stu-id="b2b4b-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b4b-116">Requirements</span></span>



| <span data-ttu-id="b2b4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b4b-117">Requirement</span></span> | <span data-ttu-id="b2b4b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b2b4b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b4b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2b4b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b2b4b-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b4b-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b2b4b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2b4b-121">Library</span></span><br/> | <dl> <span data-ttu-id="b2b4b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2b4b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2b4b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2b4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b4b-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b2b4b-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
