---
description: Define o peso de mesclagem de prioridade usado pelo controlador de animação.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'Método ID3DXAnimationController:: SetPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785154"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="129a9-103">Método ID3DXAnimationController:: SetPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="129a9-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="129a9-104">Define o peso de mesclagem de prioridade usado pelo controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="129a9-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="129a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="129a9-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="129a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="129a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129a9-107">*BlendWeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="129a9-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="129a9-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="129a9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="129a9-109">Peso de mesclagem de prioridade usado pelo controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="129a9-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129a9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="129a9-110">Return value</span></span>

<span data-ttu-id="129a9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="129a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="129a9-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="129a9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="129a9-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="129a9-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="129a9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="129a9-114">Remarks</span></span>

<span data-ttu-id="129a9-115">O peso de mistura é usado para misturar faixas de prioridade alta e baixa.</span><span class="sxs-lookup"><span data-stu-id="129a9-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="129a9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="129a9-116">Requirements</span></span>



| <span data-ttu-id="129a9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="129a9-117">Requirement</span></span> | <span data-ttu-id="129a9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="129a9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="129a9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="129a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="129a9-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="129a9-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="129a9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="129a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="129a9-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="129a9-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="129a9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="129a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129a9-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="129a9-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="129a9-125">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="129a9-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
