---
description: Fornece acesso a propriedades e métodos expostos por um objeto.
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Método CMediaEvent. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22482cffe11f62d50361bc950409858a2436d8a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754155"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="0a5ed-103">Método CMediaEvent. Invoke</span><span class="sxs-lookup"><span data-stu-id="0a5ed-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="0a5ed-104">Fornece acesso a propriedades e métodos expostos por um objeto.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a5ed-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="0a5ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a5ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a5ed-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-108">Identificador do membro.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-108">Identifier of the member.</span></span> <span data-ttu-id="0a5ed-109">Use [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md) ou a documentação do objeto para obter o identificador de expedição.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-111">Reserved for future use.</span></span> <span data-ttu-id="0a5ed-112">Deve ser um IID \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-114">Contexto de localidade no qual interpretar argumentos.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-116">Sinalizadores que descrevem o contexto da `CMediaEvent::Invoke` chamada.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-118">Ponteiro para uma estrutura que contém uma matriz de argumentos, uma matriz de IDs de expedição de argumento para argumentos nomeados e contagens para o número de elementos nas matrizes.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-120">Ponteiro para onde o resultado deve ser armazenado, ou **NULL** se o chamador não espera nenhum resultado.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-122">Ponteiro para uma estrutura que contém informações de exceção.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="0a5ed-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="0a5ed-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5ed-124">Ponteiro para o índice do primeiro argumento, dentro da matriz **rgvarg** da estrutura **DISPPARAMS** , que tem um erro.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="0a5ed-125">Para obter mais informações sobre o **DISPPARAMS**, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a5ed-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a5ed-126">Return value</span></span>

<span data-ttu-id="0a5ed-127">Retorna o DISP \_ E \_ UNKNOWNINTERFACE se *riid* não for \_ nulo como IID.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="0a5ed-128">Retorna um dos códigos de erro de [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md) se a chamada falhar.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="0a5ed-129">Caso contrário, retorna o **HRESULT** da chamada para **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="0a5ed-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5ed-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5ed-130">Requirements</span></span>



| <span data-ttu-id="0a5ed-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a5ed-131">Requirement</span></span> | <span data-ttu-id="0a5ed-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0a5ed-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5ed-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a5ed-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0a5ed-134"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a5ed-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a5ed-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a5ed-135">Library</span></span><br/> | <dl> <span data-ttu-id="0a5ed-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0a5ed-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a5ed-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a5ed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5ed-138">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="0a5ed-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




