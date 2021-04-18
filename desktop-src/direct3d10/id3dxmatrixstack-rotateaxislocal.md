---
description: Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'Método ID3DXMATRIXStack:: RotateAxisLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b00e1fd5b678d89d6b5ca4680499f6fde723c12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760246"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="5e47d-103">Método ID3DXMATRIXStack:: RotateAxisLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="5e47d-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="5e47d-104">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5e47d-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e47d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e47d-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="5e47d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e47d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e47d-107">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e47d-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e47d-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5e47d-109">Ponteiro para o eixo arbitrário de rotação.</span><span class="sxs-lookup"><span data-stu-id="5e47d-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="5e47d-110">Consulte [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="5e47d-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e47d-111">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e47d-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e47d-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e47d-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e47d-113">Ângulo de rotação sobre o eixo arbitrário, em radianos.</span><span class="sxs-lookup"><span data-stu-id="5e47d-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="5e47d-114">Os ângulos são medidos no sentido anti-horário ao examinar o eixo arbitrário em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="5e47d-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e47d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e47d-115">Return value</span></span>

<span data-ttu-id="5e47d-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e47d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e47d-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5e47d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e47d-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5e47d-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e47d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e47d-119">Remarks</span></span>

<span data-ttu-id="5e47d-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e47d-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="5e47d-121">Como a rotação é multiplicada à esquerda na pilha de matriz, a rotação é relativa ao espaço de coordenadas local do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e47d-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e47d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e47d-122">Requirements</span></span>



| <span data-ttu-id="5e47d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e47d-123">Requirement</span></span> | <span data-ttu-id="5e47d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5e47d-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e47d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e47d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5e47d-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e47d-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e47d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e47d-127">Library</span></span><br/> | <dl> <span data-ttu-id="5e47d-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e47d-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e47d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e47d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e47d-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5e47d-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5e47d-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5e47d-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
