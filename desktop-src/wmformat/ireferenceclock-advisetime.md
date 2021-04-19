---
title: Método Aconselhetime IReferenceClock
description: O método Aconselhetime solicita uma notificação assíncrona que um tempo decorreu.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Método aconselhetime Windows Media Format
- Método aconselhetime Windows Media Format, interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, método Aconselhetime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105772732"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="25ccf-106">Método IReferenceClock:: AdviseTime</span><span class="sxs-lookup"><span data-stu-id="25ccf-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="25ccf-107">O método **aconselhetime** solicita uma notificação assíncrona que um tempo decorreu.</span><span class="sxs-lookup"><span data-stu-id="25ccf-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ccf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25ccf-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="25ccf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25ccf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ccf-110">*rtBaseTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-111">Tempo de referência base, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="25ccf-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="25ccf-112">*rtStreamTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-113">Tempo de deslocamento de fluxo, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="25ccf-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="25ccf-114">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-115">Identificador para um evento, criado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="25ccf-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="25ccf-116">Esse evento será sinalizado quando o tempo especificado for decorrido.</span><span class="sxs-lookup"><span data-stu-id="25ccf-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="25ccf-117">*pdwAdviseCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-118">Ponteiro para uma variável que recebe um identificador para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="25ccf-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="25ccf-119">Isso é usado para identificar essa chamada para o **aconselhetime** no futuro, por exemplo, para cancelar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="25ccf-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ccf-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25ccf-120">Return value</span></span>

<span data-ttu-id="25ccf-121">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="25ccf-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="25ccf-122">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="25ccf-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="25ccf-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="25ccf-123">Return code</span></span>                                                                               | <span data-ttu-id="25ccf-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="25ccf-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="25ccf-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="25ccf-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="25ccf-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="25ccf-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="25ccf-128">O parâmetro *pdwAdviseCookie* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="25ccf-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="25ccf-129"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="25ccf-130">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="25ccf-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="25ccf-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="25ccf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ccf-132">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="25ccf-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





