---
description: Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.
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
ms.openlocfilehash: fe393922206744c23b534bf8d701d6292736c65a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759317"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="eef30-103">Método CMediaControl. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="eef30-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="eef30-104">Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="eef30-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eef30-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="eef30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eef30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef30-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="eef30-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="eef30-108">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="eef30-108">Type information to return.</span></span> <span data-ttu-id="eef30-109">Passe zero para recuperar informações de tipo para a implementação de **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="eef30-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="eef30-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="eef30-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="eef30-111">ID de localidade para as informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="eef30-111">Locale ID for the type information.</span></span> <span data-ttu-id="eef30-112">Para classes que dão suporte a nomes de membros localizados, um objeto poderá retornar informações de tipo diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="eef30-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="eef30-113">Para classes que não dão suporte a nomes de membros localizados, esse parâmetro pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="eef30-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="eef30-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="eef30-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="eef30-115">Endereço de um ponteiro para o objeto Type-informations solicitado.</span><span class="sxs-lookup"><span data-stu-id="eef30-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef30-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eef30-116">Return value</span></span>

<span data-ttu-id="eef30-117">Retorna um \_ ponteiro E se *ppTInfo* for inválido.</span><span class="sxs-lookup"><span data-stu-id="eef30-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="eef30-118">Retorna o tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* não for zero.</span><span class="sxs-lookup"><span data-stu-id="eef30-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="eef30-119">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="eef30-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="eef30-120">Caso contrário, retorna um **HRESULT** de uma das chamadas para recuperar o tipo.</span><span class="sxs-lookup"><span data-stu-id="eef30-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef30-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef30-121">Requirements</span></span>



| <span data-ttu-id="eef30-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef30-122">Requirement</span></span> | <span data-ttu-id="eef30-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eef30-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef30-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eef30-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eef30-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eef30-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eef30-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eef30-126">Library</span></span><br/> | <dl> <span data-ttu-id="eef30-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eef30-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef30-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eef30-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef30-129">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="eef30-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




