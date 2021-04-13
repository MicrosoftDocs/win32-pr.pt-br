---
description: Retorna a posição de hora no período de tempo local de um conjunto de animações.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Método ID3DXAnimationSet:: GetPeriodicPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298836"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="b4b66-103">Método ID3DXAnimationSet:: GetPeriodicPosition</span><span class="sxs-lookup"><span data-stu-id="b4b66-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="b4b66-104">Retorna a posição de hora no período de tempo local de um conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="b4b66-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4b66-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="b4b66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4b66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b66-107">*Posição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4b66-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b66-108">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4b66-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4b66-109">Hora local do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="b4b66-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b66-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4b66-110">Return value</span></span>

<span data-ttu-id="b4b66-111">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4b66-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4b66-112">Posição de tempo conforme medida no período do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="b4b66-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="b4b66-113">Esse valor será limitado pelo período do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="b4b66-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b66-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4b66-114">Remarks</span></span>

<span data-ttu-id="b4b66-115">A posição de tempo retornada por esse método pode ser usada como o parâmetro PeriodicPosition de [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).</span><span class="sxs-lookup"><span data-stu-id="b4b66-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4b66-116">Requirements</span></span>



| <span data-ttu-id="b4b66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b66-117">Requirement</span></span> | <span data-ttu-id="b4b66-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b4b66-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b66-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4b66-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b4b66-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b66-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b4b66-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4b66-121">Library</span></span><br/> | <dl> <span data-ttu-id="b4b66-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4b66-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4b66-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4b66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b66-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b4b66-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
