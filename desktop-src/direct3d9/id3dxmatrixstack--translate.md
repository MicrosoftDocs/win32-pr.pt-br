---
description: 'Método ID3DXMATRIXStack:: translate (D3dx9math. h) – determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'Método ID3DXMATRIXStack:: translate (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093334"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="397f3-103">Método ID3DXMATRIXStack:: translate (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="397f3-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="397f3-104">Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).</span><span class="sxs-lookup"><span data-stu-id="397f3-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="397f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="397f3-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="397f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="397f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="397f3-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="397f3-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397f3-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="397f3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="397f3-109">O fator de conversão na direção x.</span><span class="sxs-lookup"><span data-stu-id="397f3-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="397f3-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="397f3-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397f3-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="397f3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="397f3-112">O fator de conversão na direção y.</span><span class="sxs-lookup"><span data-stu-id="397f3-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="397f3-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="397f3-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397f3-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="397f3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="397f3-115">O fator de conversão na direção z.</span><span class="sxs-lookup"><span data-stu-id="397f3-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="397f3-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="397f3-116">Return value</span></span>

<span data-ttu-id="397f3-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="397f3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="397f3-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="397f3-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="397f3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="397f3-119">Remarks</span></span>

<span data-ttu-id="397f3-120">Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem do mundo atual).</span><span class="sxs-lookup"><span data-stu-id="397f3-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="397f3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="397f3-121">Requirements</span></span>



| <span data-ttu-id="397f3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="397f3-122">Requirement</span></span> | <span data-ttu-id="397f3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="397f3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="397f3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="397f3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="397f3-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="397f3-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="397f3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="397f3-126">Library</span></span><br/> | <dl> <span data-ttu-id="397f3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="397f3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="397f3-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="397f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397f3-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="397f3-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="397f3-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="397f3-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
