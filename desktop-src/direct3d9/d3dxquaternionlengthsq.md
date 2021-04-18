---
description: Retorna o quadrado do comprimento de um Quaternion.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Função D3DXQuaternionLengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764282"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="16001-103">Função D3DXQuaternionLengthSq</span><span class="sxs-lookup"><span data-stu-id="16001-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="16001-104">Retorna o quadrado do comprimento de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="16001-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="16001-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16001-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="16001-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16001-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16001-107">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16001-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16001-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="16001-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="16001-109">Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="16001-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16001-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16001-110">Return value</span></span>

<span data-ttu-id="16001-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16001-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16001-112">O comprimento quadrado do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="16001-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="16001-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="16001-113">Remarks</span></span>

<span data-ttu-id="16001-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="16001-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="16001-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16001-115">Requirements</span></span>



| <span data-ttu-id="16001-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16001-116">Requirement</span></span> | <span data-ttu-id="16001-117">Valor</span><span class="sxs-lookup"><span data-stu-id="16001-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16001-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16001-118">Header</span></span><br/>  | <dl> <span data-ttu-id="16001-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16001-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="16001-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16001-120">Library</span></span><br/> | <dl> <span data-ttu-id="16001-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16001-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16001-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="16001-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16001-123">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="16001-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="16001-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="16001-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
