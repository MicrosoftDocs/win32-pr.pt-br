---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado, até que um novo comando de execução seja emitido para o filtro. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752490"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="513cd-104">Método CRenderedInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="513cd-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="513cd-105">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado, até que um novo comando de execução seja emitido para o filtro.</span><span class="sxs-lookup"><span data-stu-id="513cd-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="513cd-106">Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="513cd-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="513cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="513cd-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="513cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="513cd-108">Parameters</span></span>

<span data-ttu-id="513cd-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="513cd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="513cd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="513cd-110">Return value</span></span>

<span data-ttu-id="513cd-111">Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="513cd-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="513cd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="513cd-112">Remarks</span></span>

<span data-ttu-id="513cd-113">Se o filtro estiver em execução, esse método enviará um evento de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="513cd-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="513cd-114">Caso contrário, é definido um sinalizador para que o \_ evento de conclusão do EC seja enviado quando o filtro for executado em seguida.</span><span class="sxs-lookup"><span data-stu-id="513cd-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="513cd-115">A liberação do filtro limpa o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="513cd-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="513cd-116">Você deve substituir esse método para manter o bloqueio de streaming do PIN:</span><span class="sxs-lookup"><span data-stu-id="513cd-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="513cd-117">Além disso, se os processos de filtro **receberem** chamadas de forma assíncrona, o PIN deverá aguardar para enviar o evento de conclusão do EC \_ até que o filtro tenha processado todas as amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="513cd-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="513cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513cd-118">Requirements</span></span>



| <span data-ttu-id="513cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="513cd-119">Requirement</span></span> | <span data-ttu-id="513cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="513cd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513cd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="513cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="513cd-122"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="513cd-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="513cd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="513cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="513cd-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="513cd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513cd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="513cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513cd-126">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="513cd-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




