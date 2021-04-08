---
description: Esquemas de Internet com suporte do WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829726"
---
# <a name="internet_scheme"></a><span data-ttu-id="f0630-103">esquema de INTERNET \_</span><span class="sxs-lookup"><span data-stu-id="f0630-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="f0630-104">Esquemas de Internet com suporte do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f0630-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="f0630-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**esquema de INTERNET \_ \_ http**</span><span class="sxs-lookup"><span data-stu-id="f0630-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0630-106">1</span><span class="sxs-lookup"><span data-stu-id="f0630-106">1</span></span>
</dt> <dt>



<span data-ttu-id="f0630-107">Um esquema de Internet HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0630-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0630-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_https de esquema de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="f0630-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0630-109">2</span><span class="sxs-lookup"><span data-stu-id="f0630-109">2</span></span>
</dt> <dt>



<span data-ttu-id="f0630-110">Um esquema de Internet HTTPS (SSL).</span><span class="sxs-lookup"><span data-stu-id="f0630-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0630-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP do esquema de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="f0630-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0630-112">3</span><span class="sxs-lookup"><span data-stu-id="f0630-112">3</span></span>
</dt> <dt>



<span data-ttu-id="f0630-113">Um esquema de Internet FTP.</span><span class="sxs-lookup"><span data-stu-id="f0630-113">An FTP internet scheme.</span></span> <span data-ttu-id="f0630-114">Esse esquema só tem suporte para uso em [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="f0630-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0630-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**esquema de INTERNET \_ \_ Socks**</span><span class="sxs-lookup"><span data-stu-id="f0630-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0630-116">4</span><span class="sxs-lookup"><span data-stu-id="f0630-116">4</span></span>
</dt> <dt>



<span data-ttu-id="f0630-117">Um esquema de Internet Socks.</span><span class="sxs-lookup"><span data-stu-id="f0630-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="f0630-118">Esse esquema só tem suporte para uso na [**\_ entrada de \_ resultado \_ do proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span><span class="sxs-lookup"><span data-stu-id="f0630-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0630-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0630-119">Requirements</span></span>



| <span data-ttu-id="f0630-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0630-120">Requirement</span></span> | <span data-ttu-id="f0630-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f0630-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0630-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0630-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0630-123">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f0630-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="f0630-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0630-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0630-125">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f0630-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="f0630-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0630-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0630-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0630-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0630-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0630-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0630-129">**\_entrada de \_ resultado do proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="f0630-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




