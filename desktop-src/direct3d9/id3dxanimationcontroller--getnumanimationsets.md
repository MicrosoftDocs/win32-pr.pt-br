---
description: Retorna o número de conjuntos de animação atualmente registrados no controlador de animação.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Método ID3DXAnimationController:: GetNumAnimationSets (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786306"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="fe4ab-103">Método ID3DXAnimationController:: GetNumAnimationSets</span><span class="sxs-lookup"><span data-stu-id="fe4ab-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="fe4ab-104">Retorna o número de conjuntos de animação atualmente registrados no controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="fe4ab-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe4ab-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="fe4ab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe4ab-106">Parameters</span></span>

<span data-ttu-id="fe4ab-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe4ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe4ab-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe4ab-108">Return value</span></span>

<span data-ttu-id="fe4ab-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe4ab-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe4ab-110">Número de conjuntos de animação.</span><span class="sxs-lookup"><span data-stu-id="fe4ab-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe4ab-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe4ab-111">Remarks</span></span>

<span data-ttu-id="fe4ab-112">O controlador contém qualquer número de conjuntos de animações e faixas.</span><span class="sxs-lookup"><span data-stu-id="fe4ab-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="fe4ab-113">Os conjuntos de animação podem ser registrados com [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span><span class="sxs-lookup"><span data-stu-id="fe4ab-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="fe4ab-114">Um controlador de animação criado por uma chamada para [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) irá registrar automaticamente os conjuntos de animação carregados.</span><span class="sxs-lookup"><span data-stu-id="fe4ab-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe4ab-115">Requirements</span></span>



| <span data-ttu-id="fe4ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe4ab-116">Requirement</span></span> | <span data-ttu-id="fe4ab-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4ab-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4ab-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe4ab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fe4ab-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ab-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fe4ab-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe4ab-120">Library</span></span><br/> | <dl> <span data-ttu-id="fe4ab-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ab-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe4ab-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe4ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4ab-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="fe4ab-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
