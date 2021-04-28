---
description: 'Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h) – gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.'
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8bb516e759e781ca3784e49253eeaddac68075bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107374"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="5de66-103">Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5de66-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="5de66-104">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5de66-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5de66-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="5de66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5de66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de66-107">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5de66-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de66-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5de66-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5de66-109">A guinada em volta do eixo y em radianos.</span><span class="sxs-lookup"><span data-stu-id="5de66-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5de66-110">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5de66-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de66-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5de66-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5de66-112">A inclinação em volta do eixo x em radianos.</span><span class="sxs-lookup"><span data-stu-id="5de66-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5de66-113">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5de66-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de66-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5de66-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5de66-115">O rolo em volta do eixo z em radianos.</span><span class="sxs-lookup"><span data-stu-id="5de66-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de66-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5de66-116">Return value</span></span>

<span data-ttu-id="5de66-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5de66-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5de66-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5de66-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de66-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5de66-119">Remarks</span></span>

<span data-ttu-id="5de66-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="5de66-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="5de66-121">Como a rotação é multiplicada à pilha da matriz, a rotação é relativa ao espaço de coordenadas do mundo.</span><span class="sxs-lookup"><span data-stu-id="5de66-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5de66-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5de66-122">Requirements</span></span>



| <span data-ttu-id="5de66-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de66-123">Requirement</span></span> | <span data-ttu-id="5de66-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5de66-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5de66-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5de66-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5de66-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de66-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5de66-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5de66-127">Library</span></span><br/> | <dl> <span data-ttu-id="5de66-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de66-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5de66-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5de66-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de66-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5de66-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5de66-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5de66-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5de66-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="5de66-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="5de66-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="5de66-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="5de66-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="5de66-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
