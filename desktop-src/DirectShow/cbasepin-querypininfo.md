---
description: 'O método QueryPinInfo recupera informações sobre o PIN. Esse método implementa o método IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749257"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="3c490-104">Método CBasePin. QueryPinInfo</span><span class="sxs-lookup"><span data-stu-id="3c490-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="3c490-105">O `QueryPinInfo` método recupera informações sobre o PIN.</span><span class="sxs-lookup"><span data-stu-id="3c490-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="3c490-106">Esse método implementa o método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="3c490-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c490-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c490-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3c490-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c490-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c490-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="3c490-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3c490-110">Ponteiro para uma estrutura de [**\_ informações de PIN**](/windows/win32/api/strmif/ns-strmif-pin_info) que recebe as informações de PIN.</span><span class="sxs-lookup"><span data-stu-id="3c490-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c490-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c490-111">Return value</span></span>

<span data-ttu-id="3c490-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3c490-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c490-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c490-113">Remarks</span></span>

<span data-ttu-id="3c490-114">Esse método usa a variável de membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) para o membro **achName** da estrutura de informações de PIN \_ .</span><span class="sxs-lookup"><span data-stu-id="3c490-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="3c490-115">Quando o método retornar, se o membro **pFilter** da estrutura de \_ informações de PIN for não **nulo**, ele terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="3c490-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="3c490-116">Certifique-se de liberar a interface quando terminar.</span><span class="sxs-lookup"><span data-stu-id="3c490-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c490-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c490-117">Requirements</span></span>



| <span data-ttu-id="3c490-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c490-118">Requirement</span></span> | <span data-ttu-id="3c490-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3c490-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c490-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c490-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3c490-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c490-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3c490-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c490-122">Library</span></span><br/> | <dl> <span data-ttu-id="3c490-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3c490-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c490-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c490-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c490-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="3c490-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




