---
description: Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'Método ID3DXMATRIXStack:: RotateAxisLocal (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8488f6314eb926495baa2e42df9ea01616131507
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790270"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="2c2c5-103">Método ID3DXMATRIXStack:: RotateAxisLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2c2c5-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="2c2c5-104">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c2c5-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="2c2c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c2c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c2c5-107">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c2c5-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2c5-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c2c5-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2c2c5-109">Ponteiro para o eixo arbitrário de rotação.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="2c2c5-110">Consulte [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="2c2c5-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2c5-111">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c2c5-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2c5-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c2c5-113">Ângulo de rotação sobre o eixo arbitrário, em radianos.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="2c2c5-114">Os ângulos são medidos no sentido anti-horário ao examinar o eixo arbitrário em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c2c5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c2c5-115">Return value</span></span>

<span data-ttu-id="2c2c5-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c2c5-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c2c5-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2c5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c2c5-119">Remarks</span></span>

<span data-ttu-id="2c2c5-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="2c2c5-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="2c2c5-121">Como a rotação é multiplicada à esquerda na pilha de matriz, a rotação é relativa ao espaço de coordenadas local do objeto.</span><span class="sxs-lookup"><span data-stu-id="2c2c5-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c2c5-122">Requirements</span></span>



| <span data-ttu-id="2c2c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c2c5-123">Requirement</span></span> | <span data-ttu-id="2c2c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2c2c5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2c5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c2c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2c2c5-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2c5-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2c2c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c2c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="2c2c5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c2c5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c2c5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c2c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2c5-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2c2c5-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2c2c5-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="2c2c5-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="2c2c5-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="2c2c5-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="2c2c5-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
