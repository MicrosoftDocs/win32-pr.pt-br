---
description: Obtém a descrição da faixa.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'Método ID3DXAnimationController:: GetTrackDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664041"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="3af62-103">Método ID3DXAnimationController:: GetTrackDesc</span><span class="sxs-lookup"><span data-stu-id="3af62-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="3af62-104">Obtém a descrição da faixa.</span><span class="sxs-lookup"><span data-stu-id="3af62-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3af62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3af62-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3af62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3af62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af62-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3af62-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af62-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3af62-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3af62-109">Identificador de faixa.</span><span class="sxs-lookup"><span data-stu-id="3af62-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3af62-110">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3af62-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3af62-111">Tipo: **[ **LPD3DXTRACK \_ desc**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="3af62-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="3af62-112">Ponteiro para a descrição da faixa.</span><span class="sxs-lookup"><span data-stu-id="3af62-112">Pointer to the track description.</span></span> <span data-ttu-id="3af62-113">Consulte [**D3DXTRACK \_ desc**](d3dxtrack-desc.md).</span><span class="sxs-lookup"><span data-stu-id="3af62-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af62-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3af62-114">Return value</span></span>

<span data-ttu-id="3af62-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3af62-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3af62-116">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3af62-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3af62-117">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3af62-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af62-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3af62-118">Requirements</span></span>



| <span data-ttu-id="3af62-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3af62-119">Requirement</span></span> | <span data-ttu-id="3af62-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3af62-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3af62-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3af62-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3af62-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3af62-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3af62-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3af62-123">Library</span></span><br/> | <dl> <span data-ttu-id="3af62-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3af62-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3af62-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3af62-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af62-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="3af62-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
