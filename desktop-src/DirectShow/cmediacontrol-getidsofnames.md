---
description: 'Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro (DISPIDs), que podem ser usados em chamadas subsequentes para a função de membro CMediaControl:: Invoke.'
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: Método CMediaControl. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750478"
---
# <a name="cmediacontrolgetidsofnames-method"></a><span data-ttu-id="3f5de-103">Método CMediaControl. GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="3f5de-103">CMediaControl.GetIDsOfNames method</span></span>

<span data-ttu-id="3f5de-104">Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro (DISPIDs), que podem ser usados em chamadas subsequentes para a função de membro [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5de-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used upon subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f5de-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="3f5de-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f5de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f5de-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="3f5de-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5de-108">Identificador de referência.</span><span class="sxs-lookup"><span data-stu-id="3f5de-108">Reference identifier.</span></span> <span data-ttu-id="3f5de-109">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3f5de-109">Reserved for future use.</span></span> <span data-ttu-id="3f5de-110">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3f5de-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f5de-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="3f5de-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5de-112">Endereço de um ponteiro para uma matriz de nomes passada para ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="3f5de-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="3f5de-113">*cNames*</span><span class="sxs-lookup"><span data-stu-id="3f5de-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5de-114">Contagem dos nomes a serem mapeados.</span><span class="sxs-lookup"><span data-stu-id="3f5de-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="3f5de-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="3f5de-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5de-116">Contexto de localidade no qual interpretar os nomes.</span><span class="sxs-lookup"><span data-stu-id="3f5de-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="3f5de-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="3f5de-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5de-118">Ponteiro para uma matriz alocada pelo chamador, cada elemento que contém uma ID correspondente a um dos nomes passados na matriz *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="3f5de-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="3f5de-119">O primeiro elemento representa o nome do membro; os elementos subsequentes representam cada um dos parâmetros do membro.</span><span class="sxs-lookup"><span data-stu-id="3f5de-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f5de-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f5de-120">Return value</span></span>

<span data-ttu-id="3f5de-121">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f5de-121">Returns one of the following values.</span></span>



| <span data-ttu-id="3f5de-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3f5de-122">Return code</span></span>                                                                                            | <span data-ttu-id="3f5de-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f5de-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f5de-124"><dt>**\_E/ \_ ou \_ CLSID desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="3f5de-125">O CLSID não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="3f5de-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="3f5de-126"><dt>**Não receber \_ E não \_ conhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="3f5de-127">Um ou mais dos nomes não eram conhecidos.</span><span class="sxs-lookup"><span data-stu-id="3f5de-127">One or more of the names were not known.</span></span> <span data-ttu-id="3f5de-128">Os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3f5de-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="3f5de-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="3f5de-130">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3f5de-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="3f5de-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="3f5de-132">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3f5de-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="3f5de-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f5de-133">Requirements</span></span>



| <span data-ttu-id="3f5de-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5de-134">Requirement</span></span> | <span data-ttu-id="3f5de-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3f5de-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5de-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f5de-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3f5de-137"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f5de-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f5de-138">Library</span></span><br/> | <dl> <span data-ttu-id="3f5de-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5de-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f5de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5de-141">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="3f5de-141">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




