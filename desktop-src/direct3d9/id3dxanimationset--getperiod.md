---
description: Obtém o período do conjunto de animações.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Método ID3DXAnimationSet:: getperiod (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105783799"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="f8a20-103">Método ID3DXAnimationSet:: getperiod</span><span class="sxs-lookup"><span data-stu-id="f8a20-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="f8a20-104">Obtém o período do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="f8a20-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8a20-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="f8a20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8a20-106">Parameters</span></span>

<span data-ttu-id="f8a20-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8a20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8a20-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8a20-108">Return value</span></span>

<span data-ttu-id="f8a20-109">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8a20-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8a20-110">Período do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="f8a20-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a20-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8a20-111">Remarks</span></span>

<span data-ttu-id="f8a20-112">O período é o intervalo de tempo em que os quadros de chave de animação são válidos.</span><span class="sxs-lookup"><span data-stu-id="f8a20-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="f8a20-113">Para animações em loop, esse é o período do loop.</span><span class="sxs-lookup"><span data-stu-id="f8a20-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="f8a20-114">As unidades de tempo em que os quadros-chave são especificados (por exemplo, segundos) são determinadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8a20-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a20-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a20-115">Requirements</span></span>



| <span data-ttu-id="f8a20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a20-116">Requirement</span></span> | <span data-ttu-id="f8a20-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a20-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a20-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8a20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f8a20-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a20-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f8a20-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8a20-120">Library</span></span><br/> | <dl> <span data-ttu-id="f8a20-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8a20-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8a20-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a20-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f8a20-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
