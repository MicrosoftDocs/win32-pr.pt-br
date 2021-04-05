---
description: Define o peso da faixa. O peso é usado para determinar como misturar várias faixas juntas.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'Método ID3DXAnimationController:: SetTrackWeight (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664110"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="a3d52-104">Método ID3DXAnimationController:: SetTrackWeight</span><span class="sxs-lookup"><span data-stu-id="a3d52-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="a3d52-105">Define o peso da faixa.</span><span class="sxs-lookup"><span data-stu-id="a3d52-105">Sets the track weight.</span></span> <span data-ttu-id="a3d52-106">O peso é usado para determinar como misturar várias faixas juntas.</span><span class="sxs-lookup"><span data-stu-id="a3d52-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d52-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d52-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="a3d52-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d52-109">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3d52-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d52-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d52-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d52-111">Identificador da faixa na qual definir o peso.</span><span class="sxs-lookup"><span data-stu-id="a3d52-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="a3d52-112">*Peso* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3d52-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d52-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d52-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d52-114">Valor de peso.</span><span class="sxs-lookup"><span data-stu-id="a3d52-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d52-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3d52-115">Return value</span></span>

<span data-ttu-id="a3d52-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3d52-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3d52-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3d52-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a3d52-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a3d52-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d52-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3d52-119">Requirements</span></span>



| <span data-ttu-id="a3d52-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d52-120">Requirement</span></span> | <span data-ttu-id="a3d52-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a3d52-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d52-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3d52-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a3d52-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d52-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a3d52-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3d52-124">Library</span></span><br/> | <dl> <span data-ttu-id="a3d52-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3d52-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3d52-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3d52-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d52-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a3d52-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
