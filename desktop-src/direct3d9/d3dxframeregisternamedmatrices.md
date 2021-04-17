---
description: Dada uma hierarquia de quadros, registra todas as matrizes nomeadas no mixer de animação.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Função D3DXFrameRegisterNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798057"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="5fcf3-103">Função D3DXFrameRegisterNamedMatrices</span><span class="sxs-lookup"><span data-stu-id="5fcf3-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="5fcf3-104">Dada uma hierarquia de quadros, registra todas as matrizes nomeadas no mixer de animação.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fcf3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fcf3-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="5fcf3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fcf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fcf3-107">*pFrameRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcf3-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcf3-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="5fcf3-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="5fcf3-109">O nó de nível superior na hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="5fcf3-110">*pAnimController* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fcf3-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcf3-111">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="5fcf3-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="5fcf3-112">Ponteiro para o objeto do controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fcf3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fcf3-113">Return value</span></span>

<span data-ttu-id="5fcf3-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fcf3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fcf3-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5fcf3-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fcf3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fcf3-117">Requirements</span></span>



| <span data-ttu-id="5fcf3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fcf3-118">Requirement</span></span> | <span data-ttu-id="5fcf3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5fcf3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcf3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fcf3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5fcf3-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fcf3-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5fcf3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fcf3-122">Library</span></span><br/> | <dl> <span data-ttu-id="5fcf3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fcf3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5fcf3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fcf3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fcf3-125">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="5fcf3-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




