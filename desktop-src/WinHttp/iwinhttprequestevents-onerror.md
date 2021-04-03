---
description: Ocorre quando há um erro em tempo de execução no aplicativo.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Evento IWinHttpRequestEvents:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922672"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="5f724-103">Evento IWinHttpRequestEvents:: OnError</span><span class="sxs-lookup"><span data-stu-id="5f724-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="5f724-104">O evento **OnError** ocorre quando há um erro em tempo de execução no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f724-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f724-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f724-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="5f724-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f724-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f724-107">*ErrorNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f724-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f724-108">Recebe o valor numérico do erro.</span><span class="sxs-lookup"><span data-stu-id="5f724-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="5f724-109">Os 16 bits inferiores desse número de erro correspondem a um dos erros listados em [**mensagens de erro**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="5f724-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f724-110">*ErrorDescription* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f724-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f724-111">Especifica uma breve descrição do erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5f724-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f724-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f724-112">Return value</span></span>

<span data-ttu-id="5f724-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5f724-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f724-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f724-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f724-115">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5f724-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f724-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f724-116">Requirements</span></span>



| <span data-ttu-id="5f724-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f724-117">Requirement</span></span> | <span data-ttu-id="5f724-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5f724-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f724-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f724-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f724-120">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="5f724-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="5f724-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f724-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f724-122">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="5f724-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="5f724-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5f724-123">Redistributable</span></span><br/>          | <span data-ttu-id="5f724-124">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5f724-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="5f724-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="5f724-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f724-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f724-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f724-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f724-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f724-128">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="5f724-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="5f724-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5f724-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="5f724-130">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5f724-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




