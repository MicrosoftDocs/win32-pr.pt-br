---
description: Método CMediaControl. GetTypeInfo – recupera um objeto Type-Information, que pode recuperar as informações de tipo de uma interface.
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Método CMediaControl. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099124"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="2c1bf-103">Método CMediaControl. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="2c1bf-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="2c1bf-104">Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c1bf-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="2c1bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c1bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c1bf-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="2c1bf-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2c1bf-108">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-108">Type information to return.</span></span> <span data-ttu-id="2c1bf-109">Passe zero para recuperar informações de tipo para a implementação de **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="2c1bf-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="2c1bf-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="2c1bf-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="2c1bf-111">ID de localidade para as informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-111">Locale ID for the type information.</span></span> <span data-ttu-id="2c1bf-112">Para classes que dão suporte a nomes de membros localizados, um objeto poderá retornar informações de tipo diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="2c1bf-113">Para classes que não dão suporte a nomes de membros localizados, esse parâmetro pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2c1bf-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="2c1bf-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2c1bf-115">Endereço de um ponteiro para o objeto Type-informations solicitado.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c1bf-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2c1bf-116">Return value</span></span>

<span data-ttu-id="2c1bf-117">Retorna um \_ ponteiro E se *ppTInfo* for inválido.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="2c1bf-118">Retorna o tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* não for zero.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="2c1bf-119">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="2c1bf-120">Caso contrário, retorna um **HRESULT** de uma das chamadas para recuperar o tipo.</span><span class="sxs-lookup"><span data-stu-id="2c1bf-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c1bf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c1bf-121">Requirements</span></span>



| <span data-ttu-id="2c1bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c1bf-122">Requirement</span></span> | <span data-ttu-id="2c1bf-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2c1bf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1bf-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c1bf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2c1bf-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c1bf-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c1bf-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c1bf-126">Library</span></span><br/> | <dl> <span data-ttu-id="2c1bf-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2c1bf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1bf-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2c1bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1bf-129">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="2c1bf-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




