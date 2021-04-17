---
description: O método CompleteConnect conclui uma conexão com outro PIN.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811758"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="ee24f-103">Método CBasePin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="ee24f-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="ee24f-104">O `CompleteConnect` método conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="ee24f-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee24f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee24f-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="ee24f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee24f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee24f-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="ee24f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="ee24f-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="ee24f-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee24f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee24f-109">Return value</span></span>

<span data-ttu-id="ee24f-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee24f-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee24f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee24f-111">Remarks</span></span>

<span data-ttu-id="ee24f-112">Esse método é chamado em ambos os Pins no final do processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="ee24f-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="ee24f-113">O PIN de conexão o chama de dentro do método [**CBasePin:: Connect**](cbasepin-connect.md) e o PIN de recebimento o chama de dentro do método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="ee24f-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="ee24f-114">Na classe base, esse método simplesmente retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee24f-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="ee24f-115">Se uma classe derivada tiver quaisquer requisitos para concluir uma conexão, ela deverá substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="ee24f-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="ee24f-116">Por exemplo, a classe [**CBaseOutputPin**](cbaseoutputpin.md) usa esse método para decidir o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="ee24f-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="ee24f-117">Se esse método falhar, a tentativa de conexão geral também falhará e o PIN desconectará do PIN de recebimento.</span><span class="sxs-lookup"><span data-stu-id="ee24f-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee24f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee24f-118">Requirements</span></span>



| <span data-ttu-id="ee24f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee24f-119">Requirement</span></span> | <span data-ttu-id="ee24f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ee24f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee24f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee24f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ee24f-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee24f-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee24f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee24f-123">Library</span></span><br/> | <dl> <span data-ttu-id="ee24f-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ee24f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee24f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee24f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee24f-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="ee24f-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




