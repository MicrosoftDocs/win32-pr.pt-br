---
description: 'Método ID3DXMATRIXStack:: Scale (D3DX10. h) – dimensione a matriz atual sobre a origem da coordenada mundial.'
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'Método ID3DXMATRIXStack:: Scale (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a7b4aceb53659fc2b1a4a95f964d068e6d7d2554
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107784"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="fe0c5-103">Método ID3DXMATRIXStack:: Scale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="fe0c5-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="fe0c5-104">Dimensione a matriz atual sobre a origem da coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe0c5-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="fe0c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe0c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0c5-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fe0c5-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0c5-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe0c5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe0c5-109">O componente de dimensionamento na direção x.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="fe0c5-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fe0c5-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0c5-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe0c5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe0c5-112">O componente de dimensionamento na direção y.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="fe0c5-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fe0c5-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0c5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe0c5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe0c5-115">O componente de dimensionamento na direção z.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0c5-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fe0c5-116">Return value</span></span>

<span data-ttu-id="fe0c5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe0c5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe0c5-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0c5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe0c5-119">Remarks</span></span>

<span data-ttu-id="fe0c5-120">Esse método multiplica a matriz atual pela matriz de escala computada.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="fe0c5-121">A transformação é sobre a origem do mundo atual.</span><span class="sxs-lookup"><span data-stu-id="fe0c5-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="fe0c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe0c5-122">Requirements</span></span>



| <span data-ttu-id="fe0c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0c5-123">Requirement</span></span> | <span data-ttu-id="fe0c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fe0c5-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0c5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe0c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fe0c5-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c5-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe0c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe0c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="fe0c5-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c5-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0c5-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fe0c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0c5-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="fe0c5-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="fe0c5-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fe0c5-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
