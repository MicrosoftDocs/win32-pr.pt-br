---
description: 'O método QueryId recupera o identificador do PIN. Esse método implementa o método IPin:: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Método CBasePin. QueryId (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754560"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="eb31e-104">Método CBasePin. QueryId</span><span class="sxs-lookup"><span data-stu-id="eb31e-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="eb31e-105">O `QueryId` método recupera o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="eb31e-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="eb31e-106">Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="eb31e-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb31e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb31e-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="eb31e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb31e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb31e-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="eb31e-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="eb31e-110">Ponteiro para o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="eb31e-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb31e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb31e-111">Return value</span></span>

<span data-ttu-id="eb31e-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb31e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eb31e-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb31e-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="eb31e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eb31e-114">Return code</span></span>                                                                                   | <span data-ttu-id="eb31e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb31e-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="eb31e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb31e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eb31e-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="eb31e-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="eb31e-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eb31e-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eb31e-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="eb31e-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="eb31e-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="eb31e-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="eb31e-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="eb31e-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb31e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb31e-122">Remarks</span></span>

<span data-ttu-id="eb31e-123">Esse método retorna uma cópia da variável de membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="eb31e-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb31e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb31e-124">Requirements</span></span>



| <span data-ttu-id="eb31e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb31e-125">Requirement</span></span> | <span data-ttu-id="eb31e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="eb31e-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb31e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb31e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eb31e-128"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb31e-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb31e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb31e-129">Library</span></span><br/> | <dl> <span data-ttu-id="eb31e-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb31e-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb31e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb31e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb31e-132">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="eb31e-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




