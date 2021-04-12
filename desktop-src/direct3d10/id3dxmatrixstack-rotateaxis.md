---
description: Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'Método ID3DXMATRIXStack:: RotateAxis (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298849"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="e2ae7-103">Método ID3DXMATRIXStack:: RotateAxis (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="e2ae7-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="e2ae7-104">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ae7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2ae7-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e2ae7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2ae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ae7-107">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2ae7-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ae7-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2ae7-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e2ae7-109">Ponteiro para o eixo arbitrário de rotação.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="e2ae7-110">Consulte [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="e2ae7-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2ae7-111">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2ae7-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ae7-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ae7-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ae7-113">Ângulo de rotação sobre o eixo arbitrário, em radianos.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="e2ae7-114">Os ângulos são medidos no sentido anti-horário ao examinar o eixo arbitrário em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ae7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2ae7-115">Return value</span></span>

<span data-ttu-id="e2ae7-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2ae7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2ae7-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e2ae7-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ae7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2ae7-119">Remarks</span></span>

<span data-ttu-id="e2ae7-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2ae7-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="e2ae7-121">Como a rotação é multiplicada à pilha da matriz, a rotação é relativa ao espaço de coordenadas do mundo.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ae7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ae7-122">Requirements</span></span>



| <span data-ttu-id="e2ae7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ae7-123">Requirement</span></span> | <span data-ttu-id="e2ae7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ae7-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ae7-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2ae7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e2ae7-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ae7-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2ae7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2ae7-127">Library</span></span><br/> | <dl> <span data-ttu-id="e2ae7-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2ae7-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ae7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2ae7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ae7-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="e2ae7-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e2ae7-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e2ae7-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
