---
description: O método GetTypeInfo recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780867"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="2b816-103">Método CMediaPosition. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="2b816-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="2b816-104">O `GetTypeInfo` método recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="2b816-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b816-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b816-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="2b816-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b816-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b816-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="2b816-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2b816-108">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="2b816-108">Type information to return.</span></span> <span data-ttu-id="2b816-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b816-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b816-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="2b816-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="2b816-111">Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="2b816-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2b816-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="2b816-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2b816-113">Endereço de uma variável que recebe um ponteiro **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="2b816-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b816-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b816-114">Return value</span></span>

<span data-ttu-id="2b816-115">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b816-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b816-116">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="2b816-116">Possible values include the following.</span></span>



| <span data-ttu-id="2b816-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2b816-117">Return code</span></span>                                                                                             | <span data-ttu-id="2b816-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b816-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2b816-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b816-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="2b816-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2b816-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="2b816-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b816-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="2b816-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="2b816-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="2b816-123"><dt>**Digite \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="2b816-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="2b816-124">O parâmetro *itinfo* não é zero.</span><span class="sxs-lookup"><span data-stu-id="2b816-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b816-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b816-125">Requirements</span></span>



| <span data-ttu-id="2b816-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b816-126">Requirement</span></span> | <span data-ttu-id="2b816-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2b816-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b816-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b816-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2b816-129"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b816-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b816-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b816-130">Library</span></span><br/> | <dl> <span data-ttu-id="2b816-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2b816-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b816-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b816-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b816-133">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="2b816-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




