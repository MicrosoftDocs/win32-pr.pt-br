---
description: Método CMediaPosition. GetTypeInfo – o método GetTypeInfo recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099134"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="5a271-103">Método CMediaPosition. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5a271-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="5a271-104">O `GetTypeInfo` método recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="5a271-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a271-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a271-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="5a271-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a271-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="5a271-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5a271-108">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="5a271-108">Type information to return.</span></span> <span data-ttu-id="5a271-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5a271-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a271-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="5a271-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="5a271-111">Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="5a271-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5a271-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="5a271-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5a271-113">Endereço de uma variável que recebe um ponteiro **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="5a271-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a271-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a271-114">Return value</span></span>

<span data-ttu-id="5a271-115">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a271-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5a271-116">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="5a271-116">Possible values include the following.</span></span>



| <span data-ttu-id="5a271-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5a271-117">Return code</span></span>                                                                                             | <span data-ttu-id="5a271-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a271-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5a271-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a271-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="5a271-120">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="5a271-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="5a271-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a271-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="5a271-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5a271-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="5a271-123"><dt>**Digite \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="5a271-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="5a271-124">O parâmetro *itinfo* não é zero.</span><span class="sxs-lookup"><span data-stu-id="5a271-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a271-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a271-125">Requirements</span></span>



| <span data-ttu-id="5a271-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a271-126">Requirement</span></span> | <span data-ttu-id="5a271-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5a271-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a271-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a271-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5a271-129"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a271-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a271-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a271-130">Library</span></span><br/> | <dl> <span data-ttu-id="5a271-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5a271-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a271-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5a271-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a271-133">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="5a271-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




