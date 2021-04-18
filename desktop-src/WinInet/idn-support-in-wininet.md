---
title: Suporte a IDN no WinINet
description: A partir do Windows Server 2008 e do Windows Vista, a parte do host da URL Unicode é convertida para o IDN (nome de domínio internacionalizado).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366577"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="a1940-103">Suporte a IDN no WinINet</span><span class="sxs-lookup"><span data-stu-id="a1940-103">IDN Support in WinINet</span></span>

<span data-ttu-id="a1940-104">A partir do Windows Server 2008 e do Windows Vista, a parte do host da URL Unicode é convertida para o IDN (nome de domínio internacionalizado).</span><span class="sxs-lookup"><span data-stu-id="a1940-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="a1940-105">Partes separadas da codificação de URL Unicode também podem ser modificadas por configurações definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1940-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="a1940-106">As versões ANSI da API do WinINet continuam a enviar a URL pela transmissão, conforme inserido pelo aplicativo, no entanto, as versões Unicode do WinINet da API agora estão em conformidade com o padrão IDN (RFC3490) para codificações de URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="a1940-107">Por padrão, quando uma URL é inserida como um parâmetro Unicode, a parte do host, para conexões diretas e proxy, é convertida no formato IDN.</span><span class="sxs-lookup"><span data-stu-id="a1940-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="a1940-108">O aplicativo tem a opção de desabilitar a formatação de host IDN definindo a opção **Internet \_ Option \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="a1940-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="a1940-109">A conversão de host IDN pode ser habilitada somente nas conexões diretas ou de proxy usando os sinalizadores de **\_ \_ \_ proxy** de IDN **\_ \_ \_ direto** ou sinalizador da Internet com a **\_ opção \_ IDNs** da Internet.</span><span class="sxs-lookup"><span data-stu-id="a1940-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="a1940-110">O exemplo de código a seguir mostra como desabilitar a conversão de host IDN para o proxy e as conexões diretas.</span><span class="sxs-lookup"><span data-stu-id="a1940-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="a1940-111">Se a formatação do host IDN estiver desabilitada, o aplicativo terá a opção de especificar a página de código desejada usando a **\_ página de \_ código da opção da Internet**.</span><span class="sxs-lookup"><span data-stu-id="a1940-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="a1940-112">O exemplo de código a seguir mostra como especificar a página de código em Japonês.</span><span class="sxs-lookup"><span data-stu-id="a1940-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="a1940-113">A parte do caminho da URL é codificada por padrão, e os segmentos restantes da URL, a consulta ou o fragmento, são convertidos na página de código padrão do sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="a1940-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="a1940-114">O exemplo a seguir mostra como especificar a página de código do idioma coreano para a parte do caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="a1940-115">A tabela a seguir define as opções que dão suporte a IDN.</span><span class="sxs-lookup"><span data-stu-id="a1940-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="a1940-116">Para obter mais informações, consulte o tópico [sinalizadores de opção](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a1940-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="a1940-117">Opção</span><span class="sxs-lookup"><span data-stu-id="a1940-117">Option</span></span>                            | <span data-ttu-id="a1940-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1940-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1940-119">página de código da \_ opção da Internet \_</span><span class="sxs-lookup"><span data-stu-id="a1940-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="a1940-120">Essa opção é definida na solicitação, ou no identificador de conexão, para especificar um esquema de codificação de página de código para a parte do host da URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="a1940-121">Essa opção será ignorada se o IDN estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="a1940-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="a1940-122">\_caminho de \_ página de código de opção da Internet \_</span><span class="sxs-lookup"><span data-stu-id="a1940-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="a1940-123">Essa opção é definida na solicitação, ou o identificador de conexão habilita o esquema de codificação especificado para a parte do caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="a1940-124">Por padrão, a parte do caminho da URL é codificada em UTF8.</span><span class="sxs-lookup"><span data-stu-id="a1940-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="a1940-125">opção de página de código de INTERNET \_ \_ \_ extra</span><span class="sxs-lookup"><span data-stu-id="a1940-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="a1940-126">Definir essa opção na solicitação ou no identificador de conexão habilita o esquema de codificação especificado para a parte extra da URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="a1940-127">Por padrão, a parte extra da URL é codificada na página de código padrão do sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="a1940-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="a1940-128">opção de INTERNET \_ \_ IDN</span><span class="sxs-lookup"><span data-stu-id="a1940-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="a1940-129">Essa opção pode ser usada na solicitação ou no identificador de conexão para habilitar ou desabilitar a conversão do host IDN.</span><span class="sxs-lookup"><span data-stu-id="a1940-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="a1940-130">Quando o IDN é desabilitado, o WinINet usa a página de código do sistema padrão para codificar a parte de host ou autoridade da URL.</span><span class="sxs-lookup"><span data-stu-id="a1940-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="a1940-131">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1940-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="a1940-132">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="a1940-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="a1940-133">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="a1940-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 