---
title: Criando o documento do serviceInfo dinamicamente
description: Criando o documento do serviceInfo dinamicamente
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Repositórios online do Windows Media Player, criando documento do serviceInfo
- lojas online, criando documento do serviceInfo
- Digite 1 lojas online, criando documento do serviceInfo
- Digite 2 lojas online, criando documento do serviceInfo
- Lojas online do Windows Media Player, criando dinamicamente o documento do serviceInfo
- lojas online, criando um documento do serviceInfo dinamicamente
- Digite 1 lojas online, criando dinamicamente o documento do serviceInfo
- tipo 2 lojas online, criando dinamicamente o documento do serviceInfo
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Criando documento do serviceInfo dinamicamente
- Criando documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915983"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="3c7f4-118">Criando o documento do serviceInfo dinamicamente</span><span class="sxs-lookup"><span data-stu-id="3c7f4-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="3c7f4-119">Você pode usar o ASP para criar seu documento do serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="3c7f4-120">Isso pode proporcionar maior flexibilidade na sua loja online usando as seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="3c7f4-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="3c7f4-121">Gerando dinamicamente o nome do host para URLs.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="3c7f4-122">Alterando URLs para localização com base nos parâmetros locale e GeoID.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="3c7f4-123">Acrescentando dinamicamente parâmetros de cadeia de caracteres de consulta da URL do serviceInfo a outras URLs, como a URL da página de navegação.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="3c7f4-124">O código de exemplo a seguir mostra uma página ASP simples que cria dinamicamente um documento do ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="3c7f4-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



<span data-ttu-id="3c7f4-125">O código de exemplo anterior usa ASP para recuperar o nome do host do servidor Web e criar dinamicamente as URLs no documento.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="3c7f4-126">O código também recupera o parâmetro de cadeia de caracteres de consulta de *localidade* da solicitação do serviceInfo e o anexa à URL da página de navegação.</span><span class="sxs-lookup"><span data-stu-id="3c7f4-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c7f4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c7f4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7f4-128">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3c7f4-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3c7f4-129">**Navegação para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3c7f4-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3c7f4-130">**Documento do serviceInfo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="3c7f4-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="3c7f4-131">**Documento do serviceInfo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3c7f4-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="3c7f4-132">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="3c7f4-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




