---
description: 'Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3DX10. h) – gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.'
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8c4f167f769a1ed46404028916477d6784e4a436
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107824"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="8c254-103">Método ID3DXMATRIXStack:: RotateYawPitchRoll (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="8c254-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="8c254-104">Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="8c254-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c254-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c254-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="8c254-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c254-107">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c254-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c254-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c254-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c254-109">A guinada em volta do eixo y em radianos.</span><span class="sxs-lookup"><span data-stu-id="8c254-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8c254-110">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c254-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c254-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c254-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c254-112">A inclinação em volta do eixo x em radianos.</span><span class="sxs-lookup"><span data-stu-id="8c254-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8c254-113">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c254-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c254-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c254-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c254-115">O rolo em volta do eixo z em radianos.</span><span class="sxs-lookup"><span data-stu-id="8c254-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c254-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8c254-116">Return value</span></span>

<span data-ttu-id="8c254-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c254-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c254-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c254-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c254-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c254-119">Remarks</span></span>

<span data-ttu-id="8c254-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="8c254-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="8c254-121">Como a rotação é multiplicada à pilha da matriz, a rotação é relativa ao espaço de coordenadas do mundo.</span><span class="sxs-lookup"><span data-stu-id="8c254-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c254-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c254-122">Requirements</span></span>



| <span data-ttu-id="8c254-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c254-123">Requirement</span></span> | <span data-ttu-id="8c254-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8c254-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c254-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c254-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8c254-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c254-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c254-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c254-127">Library</span></span><br/> | <dl> <span data-ttu-id="8c254-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c254-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c254-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8c254-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c254-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8c254-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8c254-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8c254-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
