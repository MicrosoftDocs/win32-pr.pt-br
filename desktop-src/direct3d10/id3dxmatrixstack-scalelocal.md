---
description: Dimensione a matriz atual sobre a origem do objeto.
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'Método ID3DXMATRIXStack:: ScaleLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 868aae418ebedbc54cb8f15ba4fa4e11d47c7f50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837976"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="5256d-103">Método ID3DXMATRIXStack:: ScaleLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="5256d-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="5256d-104">Dimensione a matriz atual sobre a origem do objeto.</span><span class="sxs-lookup"><span data-stu-id="5256d-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5256d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5256d-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="5256d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5256d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5256d-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5256d-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5256d-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5256d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5256d-109">O componente de dimensionamento na direção x.</span><span class="sxs-lookup"><span data-stu-id="5256d-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="5256d-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5256d-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5256d-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5256d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5256d-112">O componente de dimensionamento na direção y.</span><span class="sxs-lookup"><span data-stu-id="5256d-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="5256d-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5256d-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5256d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5256d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5256d-115">O componente de dimensionamento na direção z.</span><span class="sxs-lookup"><span data-stu-id="5256d-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5256d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5256d-116">Return value</span></span>

<span data-ttu-id="5256d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5256d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5256d-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5256d-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5256d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5256d-119">Remarks</span></span>

<span data-ttu-id="5256d-120">Esse método multiplica a matriz atual pela matriz de escala computada.</span><span class="sxs-lookup"><span data-stu-id="5256d-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="5256d-121">A transformação é sobre a origem local do objeto.</span><span class="sxs-lookup"><span data-stu-id="5256d-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="5256d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5256d-122">Requirements</span></span>



| <span data-ttu-id="5256d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5256d-123">Requirement</span></span> | <span data-ttu-id="5256d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5256d-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5256d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5256d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5256d-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5256d-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5256d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5256d-127">Library</span></span><br/> | <dl> <span data-ttu-id="5256d-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5256d-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5256d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5256d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5256d-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5256d-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5256d-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5256d-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
