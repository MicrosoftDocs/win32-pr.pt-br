---
description: Ocorre quando os dados de resposta começam a ser recebidos.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782675"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="f64b9-103">Evento IWinHttpRequestEvents:: OnResponseStart</span><span class="sxs-lookup"><span data-stu-id="f64b9-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="f64b9-104">O evento **OnResponseStart** ocorre quando os dados de resposta começam a ser recebidos.</span><span class="sxs-lookup"><span data-stu-id="f64b9-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f64b9-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="f64b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f64b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64b9-107">*Status* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f64b9-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f64b9-108">Recebe o código de status padrão retornado com os dados de resposta.</span><span class="sxs-lookup"><span data-stu-id="f64b9-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="f64b9-109">Os códigos de status são definidos no [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="f64b9-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="f64b9-110">*ContentType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f64b9-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f64b9-111">Especifica o tipo de conteúdo recebido, como "texto/HTML" ou "imagem/GIF".</span><span class="sxs-lookup"><span data-stu-id="f64b9-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f64b9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f64b9-112">Return value</span></span>

<span data-ttu-id="f64b9-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f64b9-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f64b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f64b9-114">Remarks</span></span>

<span data-ttu-id="f64b9-115">Para que esse evento ocorra, use [**abrir**](iwinhttprequest-open.md) para enviar uma conexão http no modo assíncrono e use [**Enviar**](iwinhttprequest-send.md) para enviar uma solicitação de dados a um servidor de Internet.</span><span class="sxs-lookup"><span data-stu-id="f64b9-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="f64b9-116">Esse é o primeiro evento WinHTTP a ocorrer após o [**envio**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="f64b9-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="f64b9-117">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f64b9-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f64b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f64b9-118">Requirements</span></span>



| <span data-ttu-id="f64b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f64b9-119">Requirement</span></span> | <span data-ttu-id="f64b9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f64b9-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64b9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f64b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f64b9-122">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f64b9-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="f64b9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f64b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f64b9-124">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f64b9-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="f64b9-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f64b9-125">Redistributable</span></span><br/>          | <span data-ttu-id="f64b9-126">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f64b9-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="f64b9-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="f64b9-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f64b9-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f64b9-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64b9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f64b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64b9-130">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="f64b9-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="f64b9-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f64b9-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="f64b9-132">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f64b9-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




