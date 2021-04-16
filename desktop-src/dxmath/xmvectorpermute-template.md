---
description: Permuta mudo dos componentes de dois vetores para criar um novo vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modelo XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752529"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="2339b-103">Modelo XMVectorPermute</span><span class="sxs-lookup"><span data-stu-id="2339b-103">XMVectorPermute template</span></span>

<span data-ttu-id="2339b-104">Permuta mudo dos componentes de dois vetores para criar um novo vetor.</span><span class="sxs-lookup"><span data-stu-id="2339b-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2339b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2339b-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="2339b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2339b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2339b-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="2339b-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="2339b-108">\[no \] primeiro vetor.</span><span class="sxs-lookup"><span data-stu-id="2339b-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="2339b-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="2339b-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="2339b-110">\[no \] segundo vetor.</span><span class="sxs-lookup"><span data-stu-id="2339b-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2339b-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2339b-111">Return Value</span></span>

<span data-ttu-id="2339b-112">Retorna o vetor mudo que resultou da combinação dos vetores de origem.</span><span class="sxs-lookup"><span data-stu-id="2339b-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2339b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2339b-113">Remarks</span></span>

<span data-ttu-id="2339b-114">Se todos os quatro índices fizerem referência apenas a um único vetor (ou seja, eles estão todos no intervalo de 0-3 ou todos no intervalo de 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) em vez disso para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2339b-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="2339b-115">Observe que a biblioteca faz uso de especializações de modelo em algumas plataformas para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2339b-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="2339b-116">Nem todo caso de espelho possível é implementado para esses casos especiais, portanto, prefira permudos onde o elemento X do vetor resultante vem do parâmetro v1 em vez do parâmetro v2.</span><span class="sxs-lookup"><span data-stu-id="2339b-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="2339b-117">Por exemplo, prefira usar `XMVectorPermute<0,1,4,5>(A,B);` para `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="2339b-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="2339b-118">Essa função é uma versão de modelo do [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) em que os argumentos de *mudo \** são valores de modelo.</span><span class="sxs-lookup"><span data-stu-id="2339b-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="2339b-119">As constantes do [XM \_ permudo \_](ovw-xnamath-reference-constants.md) são fornecidas para uso como valores de entrada para *permutex*,*mudo*,*PermuteZ* e *PermuteW*.</span><span class="sxs-lookup"><span data-stu-id="2339b-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="2339b-120">O `XMVectorPermute` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="2339b-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="2339b-121">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="2339b-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="2339b-122">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="2339b-122">Platform Requirements</span></span>

<span data-ttu-id="2339b-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2339b-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="2339b-124">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="2339b-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="2339b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2339b-125">Requirements</span></span>



| <span data-ttu-id="2339b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2339b-126">Requirement</span></span> | <span data-ttu-id="2339b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2339b-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2339b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2339b-128">Header</span></span><br/> | <dl> <span data-ttu-id="2339b-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="2339b-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2339b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2339b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2339b-131">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2339b-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="2339b-132">**XMVectorSwizzle**</span><span class="sxs-lookup"><span data-stu-id="2339b-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
