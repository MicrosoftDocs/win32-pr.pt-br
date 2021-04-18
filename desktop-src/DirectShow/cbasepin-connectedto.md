---
description: 'O método ConnectedTo recupera um ponteiro para o PIN conectado, se houver. Esse método implementa o método IPin:: ConnectedTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Método CBasePin. ConnectedTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771866"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="489d9-104">Método CBasePin. ConnectedTo</span><span class="sxs-lookup"><span data-stu-id="489d9-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="489d9-105">O `ConnectedTo` método recupera um ponteiro para o PIN conectado, se houver.</span><span class="sxs-lookup"><span data-stu-id="489d9-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="489d9-106">Esse método implementa o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="489d9-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="489d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="489d9-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="489d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="489d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489d9-109">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="489d9-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="489d9-110">Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="489d9-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489d9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="489d9-111">Return value</span></span>

<span data-ttu-id="489d9-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="489d9-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="489d9-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="489d9-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="489d9-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="489d9-114">Return code</span></span>                                                                                           | <span data-ttu-id="489d9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="489d9-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="489d9-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="489d9-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="489d9-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="489d9-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="489d9-119">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="489d9-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="489d9-120"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="489d9-121">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="489d9-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="489d9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="489d9-122">Remarks</span></span>

<span data-ttu-id="489d9-123">Se o método for executado com sucesso, a interface **IPin** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="489d9-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="489d9-124">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="489d9-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="489d9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="489d9-125">Requirements</span></span>



| <span data-ttu-id="489d9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="489d9-126">Requirement</span></span> | <span data-ttu-id="489d9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="489d9-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489d9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="489d9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="489d9-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="489d9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="489d9-130">Library</span></span><br/> | <dl> <span data-ttu-id="489d9-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489d9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="489d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489d9-133">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="489d9-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




