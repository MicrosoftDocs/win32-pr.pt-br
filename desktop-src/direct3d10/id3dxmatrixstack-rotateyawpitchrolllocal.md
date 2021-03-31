---
description: Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: 'Método ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a7b9e08adb7e66f78b3823c71e07fadfd561201
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664112"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a><span data-ttu-id="933c5-103">Método ID3DXMATRIXStack:: RotateYawPitchRollLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="933c5-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3DX10.h)</span></span>

<span data-ttu-id="933c5-104">Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="933c5-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="933c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="933c5-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="933c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="933c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933c5-107">*Guinada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="933c5-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="933c5-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="933c5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="933c5-109">A guinada em volta do eixo y em radianos.</span><span class="sxs-lookup"><span data-stu-id="933c5-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="933c5-110">*Pitch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="933c5-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="933c5-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="933c5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="933c5-112">A inclinação em volta do eixo x em radianos.</span><span class="sxs-lookup"><span data-stu-id="933c5-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="933c5-113">*Rolar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="933c5-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="933c5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="933c5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="933c5-115">O rolo em volta do eixo z em radianos.</span><span class="sxs-lookup"><span data-stu-id="933c5-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933c5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="933c5-116">Return value</span></span>

<span data-ttu-id="933c5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="933c5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="933c5-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="933c5-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="933c5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="933c5-119">Remarks</span></span>

<span data-ttu-id="933c5-120">Esse método adiciona a rotação à pilha de matriz com a matriz de rotação computada semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="933c5-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="933c5-121">Como a rotação é multiplicada à esquerda na pilha de matriz, a rotação é relativa ao espaço de coordenadas local do objeto.</span><span class="sxs-lookup"><span data-stu-id="933c5-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="933c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="933c5-122">Requirements</span></span>



| <span data-ttu-id="933c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="933c5-123">Requirement</span></span> | <span data-ttu-id="933c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="933c5-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="933c5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="933c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="933c5-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="933c5-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="933c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="933c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="933c5-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="933c5-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933c5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="933c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933c5-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="933c5-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="933c5-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="933c5-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
