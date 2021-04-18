---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modelo XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760588"
---
# <a name="xmmax-template"></a><span data-ttu-id="9d199-104">Modelo XMMax</span><span class="sxs-lookup"><span data-stu-id="9d199-104">XMMax template</span></span>

<span data-ttu-id="9d199-105">Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que dá suporte a uma sobrecarga de < e retorna a maior das duas instâncias.</span><span class="sxs-lookup"><span data-stu-id="9d199-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the larger one of the two instances.</span></span> <span data-ttu-id="9d199-106">O tipo de dados dos argumentos e o valor de retorno são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="9d199-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d199-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d199-107">Syntax</span></span>

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="9d199-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d199-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d199-109"><span id="a"></span><span id="A"></span>*um*</span><span class="sxs-lookup"><span data-stu-id="9d199-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="9d199-110">\[em \] especifica o primeiro de dois objetos.</span><span class="sxs-lookup"><span data-stu-id="9d199-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="9d199-111"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="9d199-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="9d199-112">\[em \] especifica os dois de dois objetos.</span><span class="sxs-lookup"><span data-stu-id="9d199-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d199-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9d199-113">Return Value</span></span>

<span data-ttu-id="9d199-114">Retorna o maior dos dois objetos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d199-114">Returns the larger of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d199-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d199-115">Remarks</span></span>

<span data-ttu-id="9d199-116">`XMMax` é um modelo e o tipo T é especificado quando o modelo é instanciado.</span><span class="sxs-lookup"><span data-stu-id="9d199-116">`XMMax` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="9d199-117">O `XMMax` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="9d199-117">The `XMMax` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="9d199-118">`XMMax` está disponível como uma macro no XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="9d199-118">`XMMax` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="9d199-119">Idealmente, use std:: Max em vez de `XMMax` .</span><span class="sxs-lookup"><span data-stu-id="9d199-119">Ideally use std::max instead of `XMMax`.</span></span> <span data-ttu-id="9d199-120">Para evitar conflitos com cabeçalhos do Windows com std:: Max, você precisa \# definir NOMINMAX antes de incluir cabeçalhos do Windows.</span><span class="sxs-lookup"><span data-stu-id="9d199-120">To avoid conflicts with Windows headers with std::max, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="9d199-121">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="9d199-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="9d199-122">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="9d199-122">Platform Requirements</span></span>

<span data-ttu-id="9d199-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d199-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="9d199-124">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="9d199-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d199-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d199-125">Requirements</span></span>



| <span data-ttu-id="9d199-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d199-126">Requirement</span></span> | <span data-ttu-id="9d199-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9d199-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d199-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d199-128">Header</span></span><br/> | <dl> <span data-ttu-id="9d199-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d199-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d199-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d199-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d199-131">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9d199-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="9d199-132">**XMMin**</span><span class="sxs-lookup"><span data-stu-id="9d199-132">**XMMin**</span></span>](xmmin-template.md)
</dt> </dl>

 

 




