---
description: Gira o vetor à esquerda por um determinado número de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modelo XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750084"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="ed46d-103">Modelo XMVectorRotateLeft</span><span class="sxs-lookup"><span data-stu-id="ed46d-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="ed46d-104">Gira o vetor à esquerda por um determinado número de elementos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ed46d-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed46d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed46d-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="ed46d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed46d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed46d-107"><span id="V"></span><span id="v"></span>*L*</span><span class="sxs-lookup"><span data-stu-id="ed46d-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="ed46d-108">\[em \] vetor para girar para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="ed46d-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed46d-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ed46d-109">Return Value</span></span>

<span data-ttu-id="ed46d-110">Retorna o [**XMVECTOR**](xmvector-data-type.md)girado.</span><span class="sxs-lookup"><span data-stu-id="ed46d-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed46d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed46d-111">Remarks</span></span>

<span data-ttu-id="ed46d-112">Essa função é uma versão de modelo do [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , em que o argumento *Elements* é um valor de modelo.</span><span class="sxs-lookup"><span data-stu-id="ed46d-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="ed46d-113">O `XMVectorRotateLeft` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="ed46d-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="ed46d-114">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="ed46d-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ed46d-115">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="ed46d-115">Platform Requirements</span></span>

<span data-ttu-id="ed46d-116">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ed46d-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ed46d-117">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ed46d-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed46d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed46d-118">Requirements</span></span>



| <span data-ttu-id="ed46d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed46d-119">Requirement</span></span> | <span data-ttu-id="ed46d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ed46d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed46d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed46d-121">Header</span></span><br/> | <dl> <span data-ttu-id="ed46d-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed46d-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed46d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed46d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed46d-124">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ed46d-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="ed46d-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="ed46d-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="ed46d-126">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="ed46d-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="ed46d-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="ed46d-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
