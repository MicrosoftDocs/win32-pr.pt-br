---
description: Método de construtor.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Construtor CSourceStream. CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750281"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="46f14-103">Construtor CSourceStream. CSourceStream</span><span class="sxs-lookup"><span data-stu-id="46f14-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="46f14-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="46f14-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f14-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46f14-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="46f14-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46f14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f14-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="46f14-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="46f14-108">Ponteiro para uma cadeia de caracteres que contém o nome de depuração do PIN.</span><span class="sxs-lookup"><span data-stu-id="46f14-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="46f14-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="46f14-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="46f14-110">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="46f14-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="46f14-111">Inicialize o valor para S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="46f14-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="46f14-112">O valor será alterado somente se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="46f14-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="46f14-113">*PMS*</span><span class="sxs-lookup"><span data-stu-id="46f14-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="46f14-114">Ponteiro para o filtro [**CSource**](csource.md) que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="46f14-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="46f14-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="46f14-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="46f14-116">Ponteiro para uma cadeia de caracteres que contém o nome do PIN.</span><span class="sxs-lookup"><span data-stu-id="46f14-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46f14-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="46f14-117">Remarks</span></span>

<span data-ttu-id="46f14-118">A cadeia de caracteres fornecida no parâmetro *pObjectName* é usada somente para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="46f14-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="46f14-119">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="46f14-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="46f14-120">A cadeia de caracteres fornecida no parâmetro *pname* é o nome retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="46f14-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="46f14-121">A `CSourceStream` classe não usa esse nome para o identificador de PIN retornado pelo método [**CSourceStream:: QueryId**](csourcestream-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="46f14-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="46f14-122">Em vez disso, **QueryId** calcula um identificador de PIN com base no número do PIN.</span><span class="sxs-lookup"><span data-stu-id="46f14-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="46f14-123">(Os identificadores de PIN dão suporte à persistência de gráfico.</span><span class="sxs-lookup"><span data-stu-id="46f14-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="46f14-124">Para obter mais informações, consulte [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span><span class="sxs-lookup"><span data-stu-id="46f14-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="46f14-125">O construtor adiciona automaticamente o PIN ao filtro proprietário, chamando [**CSource:: AddPin**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="46f14-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46f14-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f14-126">Requirements</span></span>



| <span data-ttu-id="46f14-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f14-127">Requirement</span></span> | <span data-ttu-id="46f14-128">Valor</span><span class="sxs-lookup"><span data-stu-id="46f14-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f14-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46f14-129">Header</span></span><br/>  | <dl> <span data-ttu-id="46f14-130"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46f14-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="46f14-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46f14-131">Library</span></span><br/> | <dl> <span data-ttu-id="46f14-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="46f14-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f14-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="46f14-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f14-134">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="46f14-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




