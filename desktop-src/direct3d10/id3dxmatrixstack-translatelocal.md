---
description: 'Método ID3DXMATRIXStack:: TranslateLocal (D3DX10. h) – determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.'
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'Método ID3DXMATRIXStack:: TranslateLocal (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80fabea58bd30b0db9b3ff41b522614007fe4b7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107744"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="d8772-103">Método ID3DXMATRIXStack:: TranslateLocal (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d8772-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="d8772-104">Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="d8772-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8772-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8772-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="d8772-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8772-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d8772-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8772-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8772-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8772-109">O fator de conversão na direção x.</span><span class="sxs-lookup"><span data-stu-id="d8772-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d8772-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d8772-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8772-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8772-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8772-112">O fator de conversão na direção y.</span><span class="sxs-lookup"><span data-stu-id="d8772-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d8772-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d8772-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8772-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8772-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8772-115">O fator de conversão na direção z.</span><span class="sxs-lookup"><span data-stu-id="d8772-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8772-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d8772-116">Return value</span></span>

<span data-ttu-id="d8772-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8772-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8772-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8772-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8772-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8772-119">Remarks</span></span>

<span data-ttu-id="d8772-120">Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem local do objeto).</span><span class="sxs-lookup"><span data-stu-id="d8772-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="d8772-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8772-121">Requirements</span></span>



| <span data-ttu-id="d8772-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8772-122">Requirement</span></span> | <span data-ttu-id="d8772-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d8772-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8772-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8772-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d8772-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8772-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8772-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8772-126">Library</span></span><br/> | <dl> <span data-ttu-id="d8772-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8772-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8772-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8772-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8772-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d8772-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d8772-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d8772-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
