---
description: Gira o vetor à direita por um determinado número de elementos de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modelo XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751509"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="25823-103">Modelo XMVectorRotateRight</span><span class="sxs-lookup"><span data-stu-id="25823-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="25823-104">Gira o vetor à direita por um determinado número de elementos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="25823-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="25823-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25823-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="25823-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25823-107"><span id="V"></span><span id="v"></span>*L*</span><span class="sxs-lookup"><span data-stu-id="25823-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="25823-108">\[em \] vetor para girar para a direita.</span><span class="sxs-lookup"><span data-stu-id="25823-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25823-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="25823-109">Return Value</span></span>

<span data-ttu-id="25823-110">Retorna o [**XMVECTOR**](xmvector-data-type.md)girado.</span><span class="sxs-lookup"><span data-stu-id="25823-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25823-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="25823-111">Remarks</span></span>

<span data-ttu-id="25823-112">Essa função é uma versão de modelo do [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , em que o argumento *Elements* é um valor de modelo.</span><span class="sxs-lookup"><span data-stu-id="25823-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="25823-113">O `XMVectorRotateRight` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="25823-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="25823-114">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="25823-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="25823-115">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="25823-115">Platform Requirements</span></span>

<span data-ttu-id="25823-116">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25823-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="25823-117">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="25823-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="25823-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25823-118">Requirements</span></span>



| <span data-ttu-id="25823-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25823-119">Requirement</span></span> | <span data-ttu-id="25823-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25823-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25823-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25823-121">Header</span></span><br/> | <dl> <span data-ttu-id="25823-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="25823-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25823-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="25823-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25823-124">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="25823-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="25823-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="25823-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="25823-126">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="25823-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="25823-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="25823-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
