---
description: Método CBasePin. CompleteConnect – o método CompleteConnect conclui uma conexão com outro PIN.
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096034"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="5a666-103">Método CBasePin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="5a666-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="5a666-104">O `CompleteConnect` método conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="5a666-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a666-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a666-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="5a666-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a666-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="5a666-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="5a666-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="5a666-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a666-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a666-109">Return value</span></span>

<span data-ttu-id="5a666-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a666-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a666-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a666-111">Remarks</span></span>

<span data-ttu-id="5a666-112">Esse método é chamado em ambos os Pins no final do processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="5a666-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="5a666-113">O PIN de conexão o chama de dentro do método [**CBasePin:: Connect**](cbasepin-connect.md) e o PIN de recebimento o chama de dentro do método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="5a666-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="5a666-114">Na classe base, esse método simplesmente retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a666-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="5a666-115">Se uma classe derivada tiver quaisquer requisitos para concluir uma conexão, ela deverá substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="5a666-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="5a666-116">Por exemplo, a classe [**CBaseOutputPin**](cbaseoutputpin.md) usa esse método para decidir o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="5a666-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="5a666-117">Se esse método falhar, a tentativa de conexão geral também falhará e o PIN desconectará do PIN de recebimento.</span><span class="sxs-lookup"><span data-stu-id="5a666-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a666-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a666-118">Requirements</span></span>



| <span data-ttu-id="5a666-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a666-119">Requirement</span></span> | <span data-ttu-id="5a666-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5a666-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a666-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a666-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5a666-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a666-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a666-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a666-123">Library</span></span><br/> | <dl> <span data-ttu-id="5a666-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5a666-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a666-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5a666-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a666-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5a666-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




