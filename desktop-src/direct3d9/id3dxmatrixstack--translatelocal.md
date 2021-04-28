---
description: 'Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h) – determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9badd4b01d1245247766c750e2a2ea1f266d9e1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107364"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="626ba-103">Método ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="626ba-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="626ba-104">Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="626ba-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="626ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="626ba-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="626ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="626ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="626ba-107">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="626ba-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="626ba-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="626ba-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="626ba-109">O fator de conversão na direção x.</span><span class="sxs-lookup"><span data-stu-id="626ba-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="626ba-110">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="626ba-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="626ba-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="626ba-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="626ba-112">O fator de conversão na direção y.</span><span class="sxs-lookup"><span data-stu-id="626ba-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="626ba-113">*z* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="626ba-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="626ba-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="626ba-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="626ba-115">O fator de conversão na direção z.</span><span class="sxs-lookup"><span data-stu-id="626ba-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="626ba-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="626ba-116">Return value</span></span>

<span data-ttu-id="626ba-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="626ba-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="626ba-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="626ba-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="626ba-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="626ba-119">Remarks</span></span>

<span data-ttu-id="626ba-120">Esse método multiplica a matriz atual pela matriz de conversão computada (a transformação é sobre a origem local do objeto).</span><span class="sxs-lookup"><span data-stu-id="626ba-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="626ba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="626ba-121">Requirements</span></span>



| <span data-ttu-id="626ba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="626ba-122">Requirement</span></span> | <span data-ttu-id="626ba-123">Valor</span><span class="sxs-lookup"><span data-stu-id="626ba-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="626ba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="626ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="626ba-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="626ba-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="626ba-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="626ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="626ba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="626ba-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="626ba-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="626ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626ba-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="626ba-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="626ba-130">**ID3DXMATRIXStack:: translate**</span><span class="sxs-lookup"><span data-stu-id="626ba-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
