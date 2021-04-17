---
description: Interpola entre quaternions, usando interpolação de Quadrangle esférica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Função D3DXQuaternionSquad (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759866"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="52207-103">Função D3DXQuaternionSquad (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="52207-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="52207-104">Interpola entre quaternions, usando interpolação de Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="52207-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="52207-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52207-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="52207-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52207-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="52207-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52207-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="52207-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="52207-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52207-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52207-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="52207-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52207-113">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52207-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52207-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="52207-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52207-116">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52207-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52207-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-118">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="52207-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52207-119">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52207-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52207-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-121">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="52207-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52207-122">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="52207-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52207-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52207-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52207-124">Parâmetro que indica a interpolarização entre os quaternions.</span><span class="sxs-lookup"><span data-stu-id="52207-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52207-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52207-125">Return value</span></span>

<span data-ttu-id="52207-126">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52207-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52207-127">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da interpolação quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="52207-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="52207-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="52207-128">Remarks</span></span>

<span data-ttu-id="52207-129">Essa função usa a seguinte sequência de operações de interpolação linear esférica:</span><span class="sxs-lookup"><span data-stu-id="52207-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="52207-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="52207-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="52207-131">Dessa forma, a função **D3DXQuaternionSquad** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="52207-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="52207-132">Para obter um exemplo de interpolação entre quaternions, consulte o exemplo SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="52207-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="52207-133">Você pode obter esse exemplo e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="52207-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="52207-134">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="52207-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="52207-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="52207-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="52207-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52207-136">Requirements</span></span>



| <span data-ttu-id="52207-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="52207-137">Requirement</span></span> | <span data-ttu-id="52207-138">Valor</span><span class="sxs-lookup"><span data-stu-id="52207-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52207-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52207-139">Header</span></span><br/>  | <dl> <span data-ttu-id="52207-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="52207-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="52207-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52207-141">Library</span></span><br/> | <dl> <span data-ttu-id="52207-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52207-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52207-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="52207-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52207-144">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="52207-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="52207-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="52207-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="52207-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="52207-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="52207-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="52207-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
