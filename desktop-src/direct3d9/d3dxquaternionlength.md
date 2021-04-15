---
description: Retorna o comprimento de um Quaternion.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: Função D3DXQuaternionLength (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370997"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="a0dd2-103">Função D3DXQuaternionLength</span><span class="sxs-lookup"><span data-stu-id="a0dd2-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="a0dd2-104">Retorna o comprimento de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0dd2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0dd2-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a0dd2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0dd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0dd2-107">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0dd2-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0dd2-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0dd2-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a0dd2-109">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0dd2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0dd2-110">Return value</span></span>

<span data-ttu-id="a0dd2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0dd2-112">O comprimento do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0dd2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0dd2-113">Remarks</span></span>

<span data-ttu-id="a0dd2-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0dd2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0dd2-115">Requirements</span></span>



| <span data-ttu-id="a0dd2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0dd2-116">Requirement</span></span> | <span data-ttu-id="a0dd2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a0dd2-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dd2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0dd2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a0dd2-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0dd2-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0dd2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0dd2-120">Library</span></span><br/> | <dl> <span data-ttu-id="a0dd2-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0dd2-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0dd2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0dd2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0dd2-123">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a0dd2-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a0dd2-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
