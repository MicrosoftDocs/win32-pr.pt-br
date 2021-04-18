---
description: Swizzles um vetor.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modelo XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810911"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="b3af0-103">Modelo XMVectorSwizzle</span><span class="sxs-lookup"><span data-stu-id="b3af0-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="b3af0-104">Swizzles um vetor.</span><span class="sxs-lookup"><span data-stu-id="b3af0-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3af0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3af0-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="b3af0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3af0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3af0-107"><span id="V"></span><span id="v"></span>*L*</span><span class="sxs-lookup"><span data-stu-id="b3af0-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="b3af0-108">\[em \] vetor para swizzle.</span><span class="sxs-lookup"><span data-stu-id="b3af0-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3af0-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b3af0-109">Return Value</span></span>

<span data-ttu-id="b3af0-110">Retorna o swizzled [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b3af0-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3af0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3af0-111">Remarks</span></span>

<span data-ttu-id="b3af0-112">Essa função é uma versão de modelo do [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , em que os argumentos *swizzle \** são valores de modelo.</span><span class="sxs-lookup"><span data-stu-id="b3af0-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="b3af0-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` e `XM_SWIZZLE_W` são constantes que são avaliadas como 0, 1, 2 e 3, respectivamente, para uso com `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="b3af0-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="b3af0-114">Isso é idêntico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` e `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="b3af0-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="b3af0-115">O `XMVectorSwizzle` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="b3af0-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="b3af0-116">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="b3af0-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="b3af0-117">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="b3af0-117">Platform Requirements</span></span>

<span data-ttu-id="b3af0-118">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3af0-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="b3af0-119">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="b3af0-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3af0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3af0-120">Requirements</span></span>



| <span data-ttu-id="b3af0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3af0-121">Requirement</span></span> | <span data-ttu-id="b3af0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b3af0-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3af0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3af0-123">Header</span></span><br/> | <dl> <span data-ttu-id="b3af0-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3af0-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3af0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3af0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3af0-126">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="b3af0-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="b3af0-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="b3af0-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
