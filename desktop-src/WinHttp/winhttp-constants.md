---
description: Este tópico identifica as constantes que o WinHTTP usa.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175000"
---
# <a name="winhttp-constants"></a><span data-ttu-id="04593-103">Constantes do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="04593-103">WinHTTP Constants</span></span>

<span data-ttu-id="04593-104">O WinHTTP usa as seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="04593-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="04593-105">**Mensagens de erro**</span><span class="sxs-lookup"><span data-stu-id="04593-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="04593-106">Mensagens de erro específicas para as funções do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="04593-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="04593-107">essas funções também retornam Windows mensagens de erro quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="04593-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="04593-108">O valor que corresponde a cada constante é o valor da constante para as funções da API (interface de programação de aplicativo) e os 16 bits inferiores do número do erro para o objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="04593-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="04593-109">**Códigos de status HTTP**</span><span class="sxs-lookup"><span data-stu-id="04593-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="04593-110">Constantes e valores correspondentes que indicam códigos de status HTTP retornados por servidores na Internet.</span><span class="sxs-lookup"><span data-stu-id="04593-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="04593-111">**Sinalizadores de opção**</span><span class="sxs-lookup"><span data-stu-id="04593-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="04593-112">Sinalizadores de opção com suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="04593-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="04593-113">Todos os sinalizadores de opção válidos têm um valor maior ou igual à \_ opção WinHTTP First \_ e menor ou igual à \_ última \_ opção WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="04593-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="04593-114">**porta da INTERNET \_**</span><span class="sxs-lookup"><span data-stu-id="04593-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="04593-115">Um valor de palavra que indica a porta.</span><span class="sxs-lookup"><span data-stu-id="04593-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="04593-116">**esquema de INTERNET \_**</span><span class="sxs-lookup"><span data-stu-id="04593-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="04593-117">Esquemas de Internet com suporte do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="04593-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="04593-118">**Sinalizadores de informações de consulta**</span><span class="sxs-lookup"><span data-stu-id="04593-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="04593-119">Atributos e modificadores usados por [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="04593-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="04593-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="04593-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="04593-121">Tem um valor de 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="04593-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="04593-122">Indica para [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que as cadeias de caracteres passadas são cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="04593-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="04593-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="04593-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="04593-124">Tem um valor de 0x0000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="04593-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="04593-125">Instrui o [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) a não concluir a chamada até que o buffer de dados fornecido tenha sido preenchido ou a resposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="04593-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="04593-126">Passar esse sinalizador torna o comportamento de **WinHttpReadDataEx** equivalente ao de [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="04593-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
