---
description: Determina se um Quaternion é um Quaternion de identidade.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Função D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105773002"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="8f3ec-103">Função D3DXQuaternionIsIdentity</span><span class="sxs-lookup"><span data-stu-id="8f3ec-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="8f3ec-104">Determina se um Quaternion é um Quaternion de identidade.</span><span class="sxs-lookup"><span data-stu-id="8f3ec-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f3ec-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="8f3ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f3ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3ec-107">*pQ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f3ec-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3ec-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f3ec-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8f3ec-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que será testada para identidade.</span><span class="sxs-lookup"><span data-stu-id="8f3ec-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f3ec-110">Return value</span></span>

<span data-ttu-id="8f3ec-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f3ec-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f3ec-112">Se o quaternion for uma identidade Quaternion, essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="8f3ec-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="8f3ec-113">Caso contrário, essa função retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8f3ec-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f3ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f3ec-114">Remarks</span></span>

<span data-ttu-id="8f3ec-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="8f3ec-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3ec-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3ec-116">Requirements</span></span>



| <span data-ttu-id="8f3ec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3ec-117">Requirement</span></span> | <span data-ttu-id="8f3ec-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3ec-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3ec-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f3ec-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8f3ec-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3ec-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8f3ec-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f3ec-121">Library</span></span><br/> | <dl> <span data-ttu-id="8f3ec-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f3ec-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f3ec-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f3ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3ec-124">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="8f3ec-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8f3ec-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="8f3ec-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
