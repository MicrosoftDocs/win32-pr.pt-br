---
description: Retorna o produto de ponto de dois quaternions.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Função D3DXQuaternionDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298753"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="c9ec6-103">Função D3DXQuaternionDot</span><span class="sxs-lookup"><span data-stu-id="c9ec6-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="c9ec6-104">Retorna o produto de ponto de dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ec6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9ec6-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="c9ec6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9ec6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ec6-107">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9ec6-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec6-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9ec6-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c9ec6-109">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9ec6-110">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9ec6-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec6-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9ec6-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c9ec6-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ec6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9ec6-113">Return value</span></span>

<span data-ttu-id="c9ec6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9ec6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9ec6-115">O produto dot de dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ec6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9ec6-116">Remarks</span></span>

<span data-ttu-id="c9ec6-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="c9ec6-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ec6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9ec6-118">Requirements</span></span>



| <span data-ttu-id="c9ec6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ec6-119">Requirement</span></span> | <span data-ttu-id="c9ec6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c9ec6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ec6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9ec6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9ec6-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ec6-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c9ec6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9ec6-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9ec6-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9ec6-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9ec6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9ec6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ec6-126">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c9ec6-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
