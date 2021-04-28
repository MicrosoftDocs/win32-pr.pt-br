---
description: 'Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h) – dimensione a matriz atual sobre a origem do objeto.'
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bd9f47b6c38b5ec72bcd25ecb5981859a87038b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093324"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="35a30-103">Método ID3DXMATRIXStack:: ScaleLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="35a30-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="35a30-104">Dimensione a matriz atual sobre a origem do objeto.</span><span class="sxs-lookup"><span data-stu-id="35a30-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35a30-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="35a30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35a30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a30-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="35a30-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a30-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a30-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a30-109">O componente de dimensionamento na direção x.</span><span class="sxs-lookup"><span data-stu-id="35a30-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="35a30-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="35a30-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a30-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a30-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a30-112">O componente de dimensionamento na direção y.</span><span class="sxs-lookup"><span data-stu-id="35a30-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="35a30-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="35a30-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a30-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a30-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a30-115">O componente de dimensionamento na direção z.</span><span class="sxs-lookup"><span data-stu-id="35a30-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a30-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="35a30-116">Return value</span></span>

<span data-ttu-id="35a30-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35a30-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35a30-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35a30-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a30-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="35a30-119">Remarks</span></span>

<span data-ttu-id="35a30-120">Esse método multiplica a matriz atual pela matriz de escala computada.</span><span class="sxs-lookup"><span data-stu-id="35a30-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="35a30-121">A transformação é sobre a origem local do objeto.</span><span class="sxs-lookup"><span data-stu-id="35a30-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="35a30-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35a30-122">Requirements</span></span>



| <span data-ttu-id="35a30-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a30-123">Requirement</span></span> | <span data-ttu-id="35a30-124">Valor</span><span class="sxs-lookup"><span data-stu-id="35a30-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a30-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35a30-125">Header</span></span><br/>  | <dl> <span data-ttu-id="35a30-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a30-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="35a30-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35a30-127">Library</span></span><br/> | <dl> <span data-ttu-id="35a30-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35a30-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35a30-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="35a30-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a30-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="35a30-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="35a30-131">**ID3DXMATRIXStack:: Scale**</span><span class="sxs-lookup"><span data-stu-id="35a30-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
