---
title: Elemento LOGURL
description: O elemento LOGURL instrui o Windows Media Player a enviar quaisquer dados de log para a URL especificada.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Elemento LOGURL do Windows Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761261"
---
# <a name="logurl-element"></a><span data-ttu-id="8471b-104">Elemento LOGURL</span><span class="sxs-lookup"><span data-stu-id="8471b-104">LOGURL Element</span></span>

<span data-ttu-id="8471b-105">O elemento **LogURL** instrui o Windows Media Player a enviar quaisquer dados de log para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="8471b-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="8471b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8471b-106">Attributes</span></span>

<span data-ttu-id="8471b-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="8471b-107">**HREF** (required)</span></span>

<span data-ttu-id="8471b-108">URL para um host que é capaz de processar solicitações de registro em log.</span><span class="sxs-lookup"><span data-stu-id="8471b-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8471b-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="8471b-109">Parent/Child Elements</span></span>



| <span data-ttu-id="8471b-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="8471b-110">Hierarchy</span></span>       | <span data-ttu-id="8471b-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="8471b-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="8471b-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8471b-112">Parent elements</span></span> | <span data-ttu-id="8471b-113">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="8471b-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="8471b-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8471b-114">Child elements</span></span>  | <span data-ttu-id="8471b-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8471b-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8471b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8471b-116">Remarks</span></span>

<span data-ttu-id="8471b-117">O elemento **LogURL** permite que uma lista de reprodução de metarquivo de cliente envie informações de log adicionais para os servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="8471b-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="8471b-118">As informações de log são enviadas automaticamente ao servidor de origem de uma lista de reprodução quando ela é aberta e a cada **LogURL** especificada para o elemento **ASX** , se houver alguma.</span><span class="sxs-lookup"><span data-stu-id="8471b-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="8471b-119">As informações de log também são enviadas para cada **LogURL** especificado para um elemento de **entrada** quando essa entrada é atingida.</span><span class="sxs-lookup"><span data-stu-id="8471b-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="8471b-120">A URL especificada no atributo **href** de um elemento **LogURL** deve ser o endereço de um host capaz de processar solicitações de registro em log.</span><span class="sxs-lookup"><span data-stu-id="8471b-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="8471b-121">A URL pode ser qualquer URL HTTP válida.</span><span class="sxs-lookup"><span data-stu-id="8471b-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="8471b-122">A URL também pode indicar o local de um script CGI.</span><span class="sxs-lookup"><span data-stu-id="8471b-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="8471b-123">Os únicos protocolos válidos para um elemento **LogURL** são http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8471b-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="8471b-124">Um elemento **LogURL** dentro do escopo de um elemento **ASX** é aplicável somente ao metarquivo no qual ele reside, independentemente de o metarquivo ser referenciado de outro metarquivo.</span><span class="sxs-lookup"><span data-stu-id="8471b-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="8471b-125">Um elemento **LogURL** força o envio de dados de log para todo o conteúdo transmitido de dentro de seu escopo definido e apenas para o conteúdo transmitido de dentro de seu escopo definido.</span><span class="sxs-lookup"><span data-stu-id="8471b-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="8471b-126">Os dados de log serão enviados para o servidor de origem e para todas as URLs listadas em todos os elementos **LogURL** no escopo.</span><span class="sxs-lookup"><span data-stu-id="8471b-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="8471b-127">Os dados de log serão enviados apenas uma vez para cada URL listada, mesmo que a mesma URL esteja listada mais de uma vez em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="8471b-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="8471b-128">Uma repetição de uma **entrada** resultaria em outro envio às URLs listadas.</span><span class="sxs-lookup"><span data-stu-id="8471b-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="8471b-129">Não há nenhum limite para o número de elementos **LogURL** em uma playlist de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="8471b-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="8471b-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8471b-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="8471b-131">Veja a seguir exemplos de URLs válidas.</span><span class="sxs-lookup"><span data-stu-id="8471b-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="8471b-132">URL de um aplicativo ISAPI:</span><span class="sxs-lookup"><span data-stu-id="8471b-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="8471b-133">URL de um script CGI:</span><span class="sxs-lookup"><span data-stu-id="8471b-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="8471b-134">Uma URL HTTP válida:</span><span class="sxs-lookup"><span data-stu-id="8471b-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="8471b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8471b-135">Requirements</span></span>



| <span data-ttu-id="8471b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8471b-136">Requirement</span></span> | <span data-ttu-id="8471b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8471b-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="8471b-138">Versão</span><span class="sxs-lookup"><span data-stu-id="8471b-138">Version</span></span><br/> | <span data-ttu-id="8471b-139">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8471b-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8471b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8471b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8471b-141">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8471b-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8471b-142">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8471b-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





