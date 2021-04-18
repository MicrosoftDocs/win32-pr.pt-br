---
description: Ocorre quando os dados estão disponíveis da resposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Evento IWinHttpRequestEvents:: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757346"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="2408b-103">Evento IWinHttpRequestEvents:: OnResponseDataAvailable</span><span class="sxs-lookup"><span data-stu-id="2408b-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="2408b-104">O evento **OnResponseDataAvailable** ocorre quando os dados estão disponíveis da resposta.</span><span class="sxs-lookup"><span data-stu-id="2408b-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="2408b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2408b-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="2408b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2408b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2408b-107">*Dados* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2408b-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2408b-108">Uma matriz de bytes baseada em zero que recebe os dados de resposta recebidos pelo Microsoft Windows HTTP Services (WinHTTP) até o ponto em que esse evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="2408b-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="2408b-109">Esta é uma **variante** do tipo VT da \_ matriz \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="2408b-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2408b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2408b-110">Return value</span></span>

<span data-ttu-id="2408b-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2408b-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2408b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2408b-112">Remarks</span></span>

<span data-ttu-id="2408b-113">Como os dados estão em bytes, eles devem ser convertidos em caracteres largos quando colocados em uma cadeia de caracteres de caractere largo (Unicode).</span><span class="sxs-lookup"><span data-stu-id="2408b-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="2408b-114">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2408b-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2408b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2408b-115">Requirements</span></span>



| <span data-ttu-id="2408b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2408b-116">Requirement</span></span> | <span data-ttu-id="2408b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2408b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2408b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2408b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2408b-119">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="2408b-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2408b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2408b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2408b-121">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="2408b-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2408b-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2408b-122">Redistributable</span></span><br/>          | <span data-ttu-id="2408b-123">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2408b-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2408b-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="2408b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2408b-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2408b-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2408b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2408b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2408b-127">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="2408b-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="2408b-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2408b-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2408b-129">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2408b-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




