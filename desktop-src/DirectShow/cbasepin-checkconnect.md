---
description: Método CBasePin. CheckConnect – o método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096044"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="4ced1-103">Método CBasePin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="4ced1-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="4ced1-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="4ced1-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ced1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ced1-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="4ced1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ced1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ced1-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="4ced1-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4ced1-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="4ced1-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ced1-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4ced1-109">Return value</span></span>

<span data-ttu-id="4ced1-110">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ced1-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4ced1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4ced1-111">Return code</span></span>                                                                                               | <span data-ttu-id="4ced1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ced1-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="4ced1-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ced1-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="4ced1-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="4ced1-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="4ced1-115"><dt>**VFW \_ E \_ direção inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ced1-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="4ced1-116">As direções do PIN não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="4ced1-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ced1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ced1-117">Remarks</span></span>

<span data-ttu-id="4ced1-118">Esse método é chamado em ambos os Pins no início do processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="4ced1-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="4ced1-119">O PIN de conexão o chama de dentro do método [**CBasePin:: Connect**](cbasepin-connect.md) e o PIN de recebimento o chama de dentro do método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="4ced1-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="4ced1-120">Use esse método para determinar se o PIN especificado pelo parâmetro *pPin* é adequado para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="4ced1-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="4ced1-121">A classe base retornará um erro se ambos os Pins tiverem a mesma direção (entrada ou ambas as saídas).</span><span class="sxs-lookup"><span data-stu-id="4ced1-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="4ced1-122">Classes derivadas podem substituir esse método para verificar outros recursos no PIN.</span><span class="sxs-lookup"><span data-stu-id="4ced1-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="4ced1-123">Por exemplo, a classe [**CBaseOutputPin**](cbaseoutputpin.md) consulta o pino de entrada para sua interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="4ced1-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="4ced1-124">Se esse método falhar, a conexão falhará e o PIN chamará o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4ced1-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="4ced1-125">Use **BreakConnect** para liberar todos os recursos obtidos no `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="4ced1-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="4ced1-126">Por exemplo, se `CheckConnect` o chamar o método **QueryInterface** , **BreakConnect** deverá liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="4ced1-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ced1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ced1-127">Requirements</span></span>



| <span data-ttu-id="4ced1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ced1-128">Requirement</span></span> | <span data-ttu-id="4ced1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4ced1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ced1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ced1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4ced1-131"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ced1-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ced1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ced1-132">Library</span></span><br/> | <dl> <span data-ttu-id="4ced1-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4ced1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ced1-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4ced1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ced1-135">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="4ced1-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




