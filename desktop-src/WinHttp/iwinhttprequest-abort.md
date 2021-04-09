---
description: O método Abort anula um método Send do WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'Método IWinHttpRequest:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922513"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="66aa1-103">Método IWinHttpRequest:: Abort</span><span class="sxs-lookup"><span data-stu-id="66aa1-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="66aa1-104">O método **Abort** anula um método [](about-winhttp.md) [**Send**](iwinhttprequest-send.md) do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="66aa1-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66aa1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66aa1-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="66aa1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66aa1-106">Parameters</span></span>

<span data-ttu-id="66aa1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66aa1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66aa1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66aa1-108">Return value</span></span>

<span data-ttu-id="66aa1-109">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="66aa1-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66aa1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="66aa1-110">Remarks</span></span>

<span data-ttu-id="66aa1-111">Você pode anular os métodos de [**envio**](iwinhttprequest-send.md) assíncronos e síncronos.</span><span class="sxs-lookup"><span data-stu-id="66aa1-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="66aa1-112">Para anular um método [**Send**](iwinhttprequest-send.md) síncrono, você deve chamar **Abort** de dentro de um evento [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="66aa1-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="66aa1-113">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="66aa1-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66aa1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66aa1-114">Requirements</span></span>



| <span data-ttu-id="66aa1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="66aa1-115">Requirement</span></span> | <span data-ttu-id="66aa1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="66aa1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="66aa1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66aa1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66aa1-118">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="66aa1-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="66aa1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66aa1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66aa1-120">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="66aa1-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="66aa1-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="66aa1-121">Redistributable</span></span><br/>          | <span data-ttu-id="66aa1-122">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="66aa1-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="66aa1-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="66aa1-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66aa1-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66aa1-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="66aa1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66aa1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="66aa1-126"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66aa1-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="66aa1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66aa1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66aa1-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66aa1-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="66aa1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="66aa1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66aa1-130">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="66aa1-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="66aa1-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="66aa1-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="66aa1-132">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="66aa1-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




