---
description: 'Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados nas chamadas subsequentes para a função de membro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757318"
---
# <a name="cmediaeventgetidsofnames-method"></a><span data-ttu-id="36273-103">Método CMediaEvent. GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="36273-103">CMediaEvent.GetIDsOfNames method</span></span>

<span data-ttu-id="36273-104">Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados nas chamadas subsequentes para a função de membro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="36273-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used upon subsequent calls to the [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="36273-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36273-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="36273-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36273-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="36273-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="36273-108">Identificador de referência.</span><span class="sxs-lookup"><span data-stu-id="36273-108">Reference identifier.</span></span> <span data-ttu-id="36273-109">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="36273-109">Reserved for future use.</span></span> <span data-ttu-id="36273-110">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="36273-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36273-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="36273-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="36273-112">Endereço de um ponteiro para uma matriz de nomes passada para ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="36273-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="36273-113">*cNames*</span><span class="sxs-lookup"><span data-stu-id="36273-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="36273-114">Contagem dos nomes a serem mapeados.</span><span class="sxs-lookup"><span data-stu-id="36273-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="36273-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="36273-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="36273-116">Contexto de localidade no qual interpretar os nomes.</span><span class="sxs-lookup"><span data-stu-id="36273-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="36273-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="36273-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="36273-118">Ponteiro para uma matriz alocada pelo chamador, cada elemento que contém uma ID correspondente a um dos nomes passados na matriz *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="36273-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="36273-119">O primeiro elemento representa o nome do membro; os elementos subsequentes representam cada um dos parâmetros do membro.</span><span class="sxs-lookup"><span data-stu-id="36273-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36273-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36273-120">Return value</span></span>

<span data-ttu-id="36273-121">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="36273-121">Returns one of the following values.</span></span>



| <span data-ttu-id="36273-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="36273-122">Return code</span></span>                                                                                            | <span data-ttu-id="36273-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="36273-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36273-124"><dt>**\_E/ \_ ou \_ CLSID desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="36273-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="36273-125">O CLSID não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="36273-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="36273-126"><dt>**Não receber \_ E não \_ conhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="36273-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="36273-127">Um ou mais dos nomes não eram conhecidos.</span><span class="sxs-lookup"><span data-stu-id="36273-127">One or more of the names were not known.</span></span> <span data-ttu-id="36273-128">Os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.</span><span class="sxs-lookup"><span data-stu-id="36273-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="36273-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="36273-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="36273-130">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="36273-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="36273-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36273-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="36273-132">Êxito.</span><span class="sxs-lookup"><span data-stu-id="36273-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="36273-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36273-133">Requirements</span></span>



| <span data-ttu-id="36273-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36273-134">Requirement</span></span> | <span data-ttu-id="36273-135">Valor</span><span class="sxs-lookup"><span data-stu-id="36273-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36273-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36273-136">Header</span></span><br/>  | <dl> <span data-ttu-id="36273-137"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36273-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36273-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36273-138">Library</span></span><br/> | <dl> <span data-ttu-id="36273-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="36273-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36273-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="36273-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36273-141">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="36273-141">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




