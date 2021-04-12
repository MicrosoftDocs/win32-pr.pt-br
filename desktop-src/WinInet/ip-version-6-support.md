---
title: Suporte para IP versão 6
description: A partir do IE7 e superior, o WinINet dá suporte a literais IPv6 no nome do host e ao componente de autoridade do URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Suporte para IP versão 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366519"
---
# <a name="ip-version-6-support"></a><span data-ttu-id="930d8-104">Suporte para IP versão 6</span><span class="sxs-lookup"><span data-stu-id="930d8-104">IP Version 6 Support</span></span>

<span data-ttu-id="930d8-105">A partir do IE7 e superior, o WinINet dá suporte a literais IPv6 no nome do host e ao componente de autoridade do URI.</span><span class="sxs-lookup"><span data-stu-id="930d8-105">Starting with IE7 and above, WinINet supports IPv6 literals in the hostname, and the authority component of the URI.</span></span> <span data-ttu-id="930d8-106">O WinINet também dá suporte ao uso de literais IPv6 em partes relevantes do protocolo HTTP, como no cabeçalho local.</span><span class="sxs-lookup"><span data-stu-id="930d8-106">WinINet also supports the use of IPv6 literals in relevant portions of the HTTP protocol, such as in the Location header.</span></span>

## <a name="hostname-ipv6-literals-and-uri-components"></a><span data-ttu-id="930d8-107">Literais IPv6 do hostname e componentes URI</span><span class="sxs-lookup"><span data-stu-id="930d8-107">Hostname IPv6 Literals and URI Components</span></span>

<span data-ttu-id="930d8-108">O WinINet implementa literais IPv6 de acordo com as especificações no RFC 3513.</span><span class="sxs-lookup"><span data-stu-id="930d8-108">WinINet implements IPv6 literals according to the specifications in RFC 3513.</span></span> <span data-ttu-id="930d8-109">Conforme especificado nesta RFC, os literais IPv6 em um URI devem ser colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="930d8-109">As specified in this RFC, IPv6 literals in a URI must be enclosed in brackets.</span></span> <span data-ttu-id="930d8-110">Por exemplo, https:// \[ :: 1 \] /é um URI IPv6 válido; o formulário sem colchetes ( https://::1/) não é válido.</span><span class="sxs-lookup"><span data-stu-id="930d8-110">For example, https://\[::1\]/ is a valid IPv6 URI; the form without brackets (https://::1/) is not valid.</span></span> <span data-ttu-id="930d8-111">No entanto, os literais IPv6 do nome do host que não fazem parte do URI não precisam estar entre colchetes; ambos os formulários são aceitáveis para o WinINet.</span><span class="sxs-lookup"><span data-stu-id="930d8-111">Hostname IPv6 literals that are not part of the URI, however, do not need to be enclosed in the brackets; either form is acceptable to WinINet.</span></span> <span data-ttu-id="930d8-112">Por exemplo, ":: 1" e " \[ :: 1 \] " são formas aceitáveis de literais de nome de host IPv6.</span><span class="sxs-lookup"><span data-stu-id="930d8-112">For example, both "::1" and "\[::1\]" are acceptable forms of IPv6 hostname literals.</span></span> <span data-ttu-id="930d8-113">Outras APIs, como a API do WinSock, também aceitarão os dois formulários.</span><span class="sxs-lookup"><span data-stu-id="930d8-113">Other APIs, such as the WinSock API, will also accept both forms.</span></span> <span data-ttu-id="930d8-114">Portanto, os aplicativos devem estar preparados para lidar com as duas formas de literais de nome de host IPv6.</span><span class="sxs-lookup"><span data-stu-id="930d8-114">Thus applications should be prepared to handle both forms of IPv6 hostname literals.</span></span>

## <a name="scope-id"></a><span data-ttu-id="930d8-115">ID de escopo</span><span class="sxs-lookup"><span data-stu-id="930d8-115">Scope ID</span></span>

<span data-ttu-id="930d8-116">O endereço IPv6 literal no URI pode incluir uma ID de escopo.</span><span class="sxs-lookup"><span data-stu-id="930d8-116">The IPv6 literal address in the URI may include a scope ID.</span></span> <span data-ttu-id="930d8-117">Uma ID de escopo pode ser uma ID de interface como \[ FE80:: 1% 1 \] .</span><span class="sxs-lookup"><span data-stu-id="930d8-117">A scope ID can be an interface ID such as \[FE80::1%1\].</span></span> <span data-ttu-id="930d8-118">O URI padrão, documentado em RFC 3986, não define a sintaxe para a ID do escopo e o URI é considerado não-uniforme quando a ID do escopo está presente.</span><span class="sxs-lookup"><span data-stu-id="930d8-118">The URI standard, documented in RFC 3986, does not define the syntax for the scope ID, and the URI is considered non-uniform when the scope ID is present.</span></span> <span data-ttu-id="930d8-119">No entanto, o WinINet aceita uma ID de escopo no componente de autoridade do URI e no literal do nome do host IPv6.</span><span class="sxs-lookup"><span data-stu-id="930d8-119">However, WinINet accepts a scope ID in the authority component of the URI, and in the hostname IPv6 literal.</span></span>

<span data-ttu-id="930d8-120">O caractere de porcentagem (%) no endereço IPv6 literal deve ser de porcentagem de escape quando presente no URI.</span><span class="sxs-lookup"><span data-stu-id="930d8-120">The percent character (%) in the IPv6 literal address must be percent escaped when present in the URI.</span></span> <span data-ttu-id="930d8-121">Por exemplo, a ID de escopo FE80:: 2% 3, deve aparecer no URI como "https:// \[ FE80:: 2% 253 \] /", em que %25 é o caractere de porcentagem codificada hexadecimal (%).</span><span class="sxs-lookup"><span data-stu-id="930d8-121">For example, the scope ID FE80::2%3, must appear in the URI as "https://\[FE80::2%253\]/", where %25 is the hex encoded percent character (%).</span></span> <span data-ttu-id="930d8-122">Se o aplicativo recuperar o URI de uma API Unicode, como a API [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) do Winsock, o aplicativo deverá adicionar a versão de escape do caractere de porcentagem (%) no nome do host do URI.</span><span class="sxs-lookup"><span data-stu-id="930d8-122">If the application retrieves the URI from a Unicode API, such as the Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API, the application must add the escaped version of the percent character (%) in the hostname of the URI.</span></span> <span data-ttu-id="930d8-123">Para criar a versão de escape do URI, os aplicativos chamam [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) com o parâmetro *dwFlags* definido **como \_ \_ autoridade de escape ICU** e o nome de host IPv6 especificado na estrutura de componentes da URL especificada no parâmetro *lpUrlComponents* .</span><span class="sxs-lookup"><span data-stu-id="930d8-123">To create the escaped version of the URI, applications call [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) with the *dwFlags* parameter set to **ICU\_ESCAPE\_AUTHORITY**, and the IPv6 hostname specified in the URL components structure specified in the *lpUrlComponents* parameter.</span></span>

<span data-ttu-id="930d8-124">Para todas as operações de soquetes, o WinINet usa a ID de escopo.</span><span class="sxs-lookup"><span data-stu-id="930d8-124">For all sockets operations, WinINet uses the scope ID.</span></span> <span data-ttu-id="930d8-125">No entanto, como a ID do escopo tem apenas o significado do host local, ela não é enviada como parte dos cabeçalhos do protocolo HTTP na solicitação.</span><span class="sxs-lookup"><span data-stu-id="930d8-125">However, because the scope ID has only local host significance, it is not sent as part of the HTTP protocol headers in the request.</span></span> <span data-ttu-id="930d8-126">Por exemplo, a chamada para [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) é chamada com a URL a seguir no parâmetro *lpszUrl* .</span><span class="sxs-lookup"><span data-stu-id="930d8-126">For example, the call to [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) is called with the following URL in the *lpszUrl* parameter.</span></span>

``` syntax
https://[fec0::2%251]:80/path.htm
```

<span data-ttu-id="930d8-127">A parte da ID do escopo da URL é removida pelo WinINet quando a solicitação HTTP é enviada para essa URL.</span><span class="sxs-lookup"><span data-stu-id="930d8-127">The scope ID portion of the URL is removed by WinINet when the HTTP request is sent for this URL.</span></span> <span data-ttu-id="930d8-128">A solicitação contém os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="930d8-128">The request contains the following headers:</span></span>

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> <span data-ttu-id="930d8-129">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="930d8-129">WinINet does not support server implementations.</span></span> <span data-ttu-id="930d8-130">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="930d8-130">In addition, it should not be used from a service.</span></span> <span data-ttu-id="930d8-131">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="930d8-131">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 