---
description: Método CMediaPosition. GetIDsOfNames – o método GetIDsOfNames mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095524"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="fec1a-103">Método CMediaPosition. GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="fec1a-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="fec1a-104">O `GetIDsOfNames` método mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="fec1a-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fec1a-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="fec1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fec1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec1a-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="fec1a-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1a-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fec1a-108">Reserved.</span></span> <span data-ttu-id="fec1a-109">Use o IID \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="fec1a-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="fec1a-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="fec1a-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1a-111">Endereço de uma matriz de cadeias de caracteres largos que contêm os nomes a serem mapeados.</span><span class="sxs-lookup"><span data-stu-id="fec1a-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="fec1a-112">*cNames*</span><span class="sxs-lookup"><span data-stu-id="fec1a-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1a-113">Tamanho da matriz fornecida pelo parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="fec1a-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fec1a-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="fec1a-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1a-115">Contexto de localidade no qual interpretar os nomes.</span><span class="sxs-lookup"><span data-stu-id="fec1a-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="fec1a-116">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fec1a-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fec1a-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="fec1a-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1a-118">Ponteiro para uma matriz que recebe os DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="fec1a-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="fec1a-119">Cada elemento de recebe um identificador que corresponde a um dos nomes passados no parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="fec1a-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec1a-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fec1a-120">Return value</span></span>

<span data-ttu-id="fec1a-121">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fec1a-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fec1a-122">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="fec1a-122">Possible values include the following.</span></span>



| <span data-ttu-id="fec1a-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fec1a-123">Return code</span></span>                                                                                         | <span data-ttu-id="fec1a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="fec1a-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="fec1a-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fec1a-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="fec1a-126">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="fec1a-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fec1a-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fec1a-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="fec1a-128">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="fec1a-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="fec1a-129"><dt>**Não receber \_ E não \_ conhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="fec1a-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="fec1a-130">Um ou mais dos nomes não eram conhecidos.</span><span class="sxs-lookup"><span data-stu-id="fec1a-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fec1a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec1a-131">Requirements</span></span>



| <span data-ttu-id="fec1a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec1a-132">Requirement</span></span> | <span data-ttu-id="fec1a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="fec1a-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec1a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fec1a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fec1a-135"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fec1a-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fec1a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fec1a-136">Library</span></span><br/> | <dl> <span data-ttu-id="fec1a-137"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fec1a-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec1a-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fec1a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec1a-139">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="fec1a-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




