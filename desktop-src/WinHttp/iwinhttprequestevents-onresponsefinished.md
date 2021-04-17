---
description: Ocorre quando os dados da resposta são concluídos.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Evento IWinHttpRequestEvents:: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791472"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="4ca78-103">Evento IWinHttpRequestEvents:: OnResponseFinished</span><span class="sxs-lookup"><span data-stu-id="4ca78-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="4ca78-104">O evento **OnResponseFinished** ocorre quando os dados da resposta são concluídos.</span><span class="sxs-lookup"><span data-stu-id="4ca78-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca78-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="4ca78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca78-106">Parameters</span></span>

<span data-ttu-id="4ca78-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ca78-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ca78-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ca78-108">Return value</span></span>

<span data-ttu-id="4ca78-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ca78-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca78-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca78-110">Remarks</span></span>

<span data-ttu-id="4ca78-111">Esse evento sinaliza que todos os dados de resposta que pertencem à solicitação mais recente foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="4ca78-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="4ca78-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) não ocorre novamente até a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="4ca78-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="4ca78-113">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4ca78-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ca78-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca78-114">Requirements</span></span>



| <span data-ttu-id="4ca78-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca78-115">Requirement</span></span> | <span data-ttu-id="4ca78-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca78-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca78-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca78-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca78-118">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="4ca78-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4ca78-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca78-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca78-120">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="4ca78-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4ca78-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4ca78-121">Redistributable</span></span><br/>          | <span data-ttu-id="4ca78-122">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4ca78-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4ca78-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="4ca78-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ca78-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ca78-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca78-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca78-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca78-126">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="4ca78-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="4ca78-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4ca78-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4ca78-128">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ca78-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




