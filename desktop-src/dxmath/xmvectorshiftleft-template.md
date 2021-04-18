---
description: Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos vagados com elementos de um segundo vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modelo XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752734"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="1ed42-103">Modelo XMVectorShiftLeft</span><span class="sxs-lookup"><span data-stu-id="1ed42-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="1ed42-104">Desloca um vetor à esquerda por um determinado número de elementos de 32 bits, preenchendo os elementos vagados com elementos de um segundo vetor.</span><span class="sxs-lookup"><span data-stu-id="1ed42-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ed42-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="1ed42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed42-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="1ed42-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="1ed42-108">\[em \] vetor para deslocar para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="1ed42-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="1ed42-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="1ed42-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="1ed42-110">\[em \] vetor usado para preencher os componentes vagados do v1 depois que ele é deslocado para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="1ed42-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed42-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1ed42-111">Return Value</span></span>

<span data-ttu-id="1ed42-112">Retorna a mudança e a preenchida em [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1ed42-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed42-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ed42-113">Remarks</span></span>

<span data-ttu-id="1ed42-114">Essa função é uma versão de modelo do [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , em que o argumento *Elements* é um valor de modelo.</span><span class="sxs-lookup"><span data-stu-id="1ed42-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="1ed42-115">O `XMVectorShiftLeft` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="1ed42-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="1ed42-116">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="1ed42-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="1ed42-117">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="1ed42-117">Platform Requirements</span></span>

<span data-ttu-id="1ed42-118">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1ed42-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="1ed42-119">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="1ed42-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed42-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed42-120">Requirements</span></span>



| <span data-ttu-id="1ed42-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed42-121">Requirement</span></span> | <span data-ttu-id="1ed42-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed42-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed42-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ed42-123">Header</span></span><br/> | <dl> <span data-ttu-id="1ed42-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed42-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed42-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ed42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed42-126">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="1ed42-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="1ed42-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="1ed42-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="1ed42-128">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="1ed42-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="1ed42-129">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="1ed42-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
