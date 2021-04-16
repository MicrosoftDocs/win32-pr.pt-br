---
description: Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que oferece suporte a uma sobrecarga de < e retorna a menor das duas instâncias. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modelo XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782426"
---
# <a name="xmmin-template"></a><span data-ttu-id="20f8d-104">Modelo XMMin</span><span class="sxs-lookup"><span data-stu-id="20f8d-104">XMMin template</span></span>

<span data-ttu-id="20f8d-105">Compara duas instâncias de tipo de dados numéricos ou duas instâncias de um objeto que oferece suporte a uma sobrecarga de < e retorna a menor das duas instâncias.</span><span class="sxs-lookup"><span data-stu-id="20f8d-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="20f8d-106">O tipo de dados dos argumentos e o valor de retorno são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="20f8d-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f8d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20f8d-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="20f8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20f8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f8d-109"><span id="a"></span><span id="A"></span>*um*</span><span class="sxs-lookup"><span data-stu-id="20f8d-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="20f8d-110">\[em \] especifica o primeiro de dois objetos.</span><span class="sxs-lookup"><span data-stu-id="20f8d-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="20f8d-111"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="20f8d-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="20f8d-112">\[em \] especifica os dois de dois objetos.</span><span class="sxs-lookup"><span data-stu-id="20f8d-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f8d-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="20f8d-113">Return Value</span></span>

<span data-ttu-id="20f8d-114">Retorna o menor dos dois objetos de entrada.</span><span class="sxs-lookup"><span data-stu-id="20f8d-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="20f8d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="20f8d-115">Remarks</span></span>

<span data-ttu-id="20f8d-116">`XMMin` é um modelo e o tipo T é especificado quando o modelo é instanciado.</span><span class="sxs-lookup"><span data-stu-id="20f8d-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="20f8d-117">O `XMMin` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="20f8d-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="20f8d-118">`XMMin` está disponível como uma macro no XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="20f8d-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="20f8d-119">Idealmente, use std:: min em vez de `XMMin` .</span><span class="sxs-lookup"><span data-stu-id="20f8d-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="20f8d-120">Para evitar conflitos com cabeçalhos do Windows com std:: min, você precisa \# definir NOMINMAX antes de incluir cabeçalhos do Windows.</span><span class="sxs-lookup"><span data-stu-id="20f8d-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="20f8d-121">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="20f8d-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="20f8d-122">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="20f8d-122">Platform Requirements</span></span>

<span data-ttu-id="20f8d-123">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20f8d-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="20f8d-124">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="20f8d-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f8d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f8d-125">Requirements</span></span>



| <span data-ttu-id="20f8d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f8d-126">Requirement</span></span> | <span data-ttu-id="20f8d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="20f8d-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f8d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f8d-128">Header</span></span><br/> | <dl> <span data-ttu-id="20f8d-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f8d-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f8d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f8d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f8d-131">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="20f8d-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="20f8d-132">**XMMax**</span><span class="sxs-lookup"><span data-stu-id="20f8d-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




