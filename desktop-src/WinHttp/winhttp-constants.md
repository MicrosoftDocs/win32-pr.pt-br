---
description: Este tópico identifica as constantes que o WinHTTP usa.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7c277b4235e23254000766fdef53d25f19ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461126"
---
# <a name="winhttp-constants"></a><span data-ttu-id="b4e78-103">Constantes do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b4e78-103">WinHTTP Constants</span></span>

<span data-ttu-id="b4e78-104">O WinHTTP usa as seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="b4e78-104">WinHTTP uses the following constants:</span></span>

<dl> <dt>

[<span data-ttu-id="b4e78-105">**Mensagens de erro**</span><span class="sxs-lookup"><span data-stu-id="b4e78-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="b4e78-106">Mensagens de erro específicas para as funções do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b4e78-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="b4e78-107">Essas funções também retornam mensagens de erro do Windows quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="b4e78-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="b4e78-108">O valor que corresponde a cada constante é o valor da constante para as funções da API (interface de programação de aplicativo) e os 16 bits inferiores do número do erro para o objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e78-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="b4e78-109">**Códigos de status HTTP**</span><span class="sxs-lookup"><span data-stu-id="b4e78-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="b4e78-110">Constantes e valores correspondentes que indicam códigos de status HTTP retornados por servidores na Internet.</span><span class="sxs-lookup"><span data-stu-id="b4e78-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="b4e78-111">**Sinalizadores de opção**</span><span class="sxs-lookup"><span data-stu-id="b4e78-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="b4e78-112">Sinalizadores de opção com suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="b4e78-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="b4e78-113">Todos os sinalizadores de opção válidos têm um valor maior ou igual à \_ opção WinHTTP First \_ e menor ou igual à \_ última \_ opção WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b4e78-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="b4e78-114">**porta da INTERNET \_**</span><span class="sxs-lookup"><span data-stu-id="b4e78-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="b4e78-115">Um valor de palavra que indica a porta.</span><span class="sxs-lookup"><span data-stu-id="b4e78-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="b4e78-116">**esquema de INTERNET \_**</span><span class="sxs-lookup"><span data-stu-id="b4e78-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="b4e78-117">Esquemas de Internet com suporte do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b4e78-117">Internet schemes supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="b4e78-118">**Sinalizadores de informações de consulta**</span><span class="sxs-lookup"><span data-stu-id="b4e78-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt> <dd>

<span data-ttu-id="b4e78-119">Atributos e modificadores usados por [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="b4e78-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

</dd> </dl>

 

 



