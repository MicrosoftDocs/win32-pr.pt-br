---
description: Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770287"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="1d2db-103">Método CMediaEvent. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="1d2db-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="1d2db-104">Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="1d2db-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d2db-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="1d2db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2db-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="1d2db-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2db-108">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="1d2db-108">Type information to return.</span></span> <span data-ttu-id="1d2db-109">Passe zero para recuperar informações de tipo para a implementação de **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="1d2db-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="1d2db-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="1d2db-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2db-111">ID de localidade para as informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="1d2db-111">Locale ID for the type information.</span></span> <span data-ttu-id="1d2db-112">Para classes que dão suporte a nomes de membros localizados, um objeto poderá retornar informações de tipo diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="1d2db-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="1d2db-113">Para classes que não dão suporte a nomes de membros localizados, esse parâmetro pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="1d2db-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1d2db-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="1d2db-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1d2db-115">Endereço de um ponteiro para o objeto Type-informations solicitado.</span><span class="sxs-lookup"><span data-stu-id="1d2db-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2db-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d2db-116">Return value</span></span>

<span data-ttu-id="1d2db-117">Retorna um \_ ponteiro E se *ppTInfo* for inválido.</span><span class="sxs-lookup"><span data-stu-id="1d2db-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="1d2db-118">Retorna o tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* não for zero.</span><span class="sxs-lookup"><span data-stu-id="1d2db-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="1d2db-119">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1d2db-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="1d2db-120">Caso contrário, retorna um **HRESULT** de uma das chamadas para recuperar o tipo.</span><span class="sxs-lookup"><span data-stu-id="1d2db-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2db-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2db-121">Requirements</span></span>



| <span data-ttu-id="1d2db-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2db-122">Requirement</span></span> | <span data-ttu-id="1d2db-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2db-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2db-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d2db-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d2db-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d2db-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d2db-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d2db-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d2db-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d2db-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2db-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d2db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2db-129">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="1d2db-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




