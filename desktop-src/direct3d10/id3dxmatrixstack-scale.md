---
description: Dimensione a matriz atual sobre a origem da coordenada mundial.
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
ms.openlocfilehash: 361c1fcbdc3f793bcf3e21d569eee740ca0b4ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796235"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="82cf6-103">Método ID3DXMATRIXStack:: Scale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="82cf6-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="82cf6-104">Dimensione a matriz atual sobre a origem da coordenada mundial.</span><span class="sxs-lookup"><span data-stu-id="82cf6-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="82cf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82cf6-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="82cf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82cf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82cf6-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="82cf6-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82cf6-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82cf6-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82cf6-109">O componente de dimensionamento na direção x.</span><span class="sxs-lookup"><span data-stu-id="82cf6-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="82cf6-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="82cf6-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82cf6-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82cf6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82cf6-112">O componente de dimensionamento na direção y.</span><span class="sxs-lookup"><span data-stu-id="82cf6-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="82cf6-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="82cf6-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82cf6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82cf6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82cf6-115">O componente de dimensionamento na direção z.</span><span class="sxs-lookup"><span data-stu-id="82cf6-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82cf6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82cf6-116">Return value</span></span>

<span data-ttu-id="82cf6-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82cf6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82cf6-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82cf6-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="82cf6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="82cf6-119">Remarks</span></span>

<span data-ttu-id="82cf6-120">Esse método multiplica a matriz atual pela matriz de escala computada.</span><span class="sxs-lookup"><span data-stu-id="82cf6-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="82cf6-121">A transformação é sobre a origem do mundo atual.</span><span class="sxs-lookup"><span data-stu-id="82cf6-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="82cf6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82cf6-122">Requirements</span></span>



| <span data-ttu-id="82cf6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82cf6-123">Requirement</span></span> | <span data-ttu-id="82cf6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="82cf6-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82cf6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82cf6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="82cf6-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="82cf6-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="82cf6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82cf6-127">Library</span></span><br/> | <dl> <span data-ttu-id="82cf6-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82cf6-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cf6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="82cf6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cf6-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="82cf6-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="82cf6-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="82cf6-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
