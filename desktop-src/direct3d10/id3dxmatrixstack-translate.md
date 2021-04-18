---
description: Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'Método ID3DXMATRIXStack:: translate (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764413"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="3e29e-103">Método ID3DXMATRIXStack:: translate (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="3e29e-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="3e29e-104">Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).</span><span class="sxs-lookup"><span data-stu-id="3e29e-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e29e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e29e-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="3e29e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e29e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e29e-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3e29e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e29e-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e29e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e29e-109">O fator de conversão na direção x.</span><span class="sxs-lookup"><span data-stu-id="3e29e-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3e29e-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3e29e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e29e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e29e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e29e-112">O fator de conversão na direção y.</span><span class="sxs-lookup"><span data-stu-id="3e29e-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3e29e-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3e29e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e29e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e29e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e29e-115">O fator de conversão na direção z.</span><span class="sxs-lookup"><span data-stu-id="3e29e-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e29e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e29e-116">Return value</span></span>

<span data-ttu-id="3e29e-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e29e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e29e-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e29e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e29e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e29e-119">Remarks</span></span>

<span data-ttu-id="3e29e-120">Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem do mundo atual).</span><span class="sxs-lookup"><span data-stu-id="3e29e-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="3e29e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e29e-121">Requirements</span></span>



| <span data-ttu-id="3e29e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e29e-122">Requirement</span></span> | <span data-ttu-id="3e29e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3e29e-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e29e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e29e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e29e-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e29e-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e29e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e29e-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e29e-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e29e-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e29e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e29e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e29e-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="3e29e-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="3e29e-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3e29e-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
