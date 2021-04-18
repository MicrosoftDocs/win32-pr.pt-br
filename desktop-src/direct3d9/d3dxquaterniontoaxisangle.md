---
description: Computa o eixo de um Quaternion e o ângulo de rotação.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Função D3DXQuaternionToAxisAngle (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762180"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="2e61b-103">Função D3DXQuaternionToAxisAngle (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2e61b-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="2e61b-104">Computa o eixo de um Quaternion e o ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="2e61b-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e61b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e61b-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="2e61b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e61b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e61b-107">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e61b-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e61b-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e61b-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e61b-109">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="2e61b-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e61b-110">*pAxis* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2e61b-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e61b-111">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e61b-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2e61b-112">Essa função retorna um ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que identifica o eixo de rotação do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="2e61b-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="2e61b-113">*pAngle* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2e61b-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e61b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e61b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e61b-115">Essa função retorna um ponteiro para um valor FLOAT que identifica o ângulo de rotação de Quaternion em radianos.</span><span class="sxs-lookup"><span data-stu-id="2e61b-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e61b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e61b-116">Return value</span></span>

<span data-ttu-id="2e61b-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2e61b-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e61b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e61b-118">Remarks</span></span>

<span data-ttu-id="2e61b-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="2e61b-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e61b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e61b-120">Requirements</span></span>



| <span data-ttu-id="2e61b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e61b-121">Requirement</span></span> | <span data-ttu-id="2e61b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2e61b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e61b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e61b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2e61b-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e61b-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e61b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e61b-125">Library</span></span><br/> | <dl> <span data-ttu-id="2e61b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e61b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e61b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e61b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e61b-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="2e61b-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
