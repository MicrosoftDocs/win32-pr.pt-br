---
description: Retorna o quaternion da identidade.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: Função D3DXQuaternionIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298578"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="fdb01-103">Função D3DXQuaternionIdentity</span><span class="sxs-lookup"><span data-stu-id="fdb01-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="fdb01-104">Retorna o quaternion da identidade.</span><span class="sxs-lookup"><span data-stu-id="fdb01-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdb01-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="fdb01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdb01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb01-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fdb01-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb01-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb01-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fdb01-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fdb01-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb01-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdb01-110">Return value</span></span>

<span data-ttu-id="fdb01-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fdb01-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fdb01-112">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é a identidade Quaternion.</span><span class="sxs-lookup"><span data-stu-id="fdb01-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb01-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdb01-113">Remarks</span></span>

<span data-ttu-id="fdb01-114">Dado um Quaternion (x, y, z, w), a função **D3DXQuaternionIdentity** retornará o quaternion (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="fdb01-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="fdb01-115">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="fdb01-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fdb01-116">Dessa forma, a função **D3DXQuaternionIdentity** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fdb01-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fdb01-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="fdb01-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb01-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdb01-118">Requirements</span></span>



| <span data-ttu-id="fdb01-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdb01-119">Requirement</span></span> | <span data-ttu-id="fdb01-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fdb01-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb01-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdb01-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb01-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb01-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb01-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdb01-123">Library</span></span><br/> | <dl> <span data-ttu-id="fdb01-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb01-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdb01-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdb01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb01-126">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fdb01-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fdb01-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="fdb01-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




