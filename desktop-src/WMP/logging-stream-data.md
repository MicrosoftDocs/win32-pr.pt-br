---
title: Log de dados de fluxo
description: Log de dados de fluxo
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Listas de reprodução do metarquivo do Windows Media, log de dados de fluxo
- listas de reprodução, log de dados de fluxo
- listas de reprodução de metarquivo, log de dados de fluxo
- Playlists do metarquivo do Windows Media, log de dados de fluxo
- listas de reprodução, log de dados de fluxo
- playlists de metarquivo, log de dados de fluxo
- log de dados de fluxo
- log de dados de fluxo
- Windows Media Player, log de dados de fluxo
- Windows Media Player, log de dados de fluxo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084129"
---
# <a name="logging-stream-data"></a><span data-ttu-id="cf218-113">Log de dados de fluxo</span><span class="sxs-lookup"><span data-stu-id="cf218-113">Logging Stream Data</span></span>

<span data-ttu-id="cf218-114">As informações registradas podem ser adquiridas e usadas para determinar o comportamento do visualizador, por exemplo, com que frequência um fluxo é exibido ou se um usuário específico exibiu um fluxo e por quanto tempo a qualidade.</span><span class="sxs-lookup"><span data-stu-id="cf218-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="cf218-115">As informações de log são enviadas automaticamente para o servidor do qual a lista de reprodução foi originada.</span><span class="sxs-lookup"><span data-stu-id="cf218-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="cf218-116">Você também pode enviar informações de log para servidores adicionais, incluindo servidores Web que você usa exclusivamente para registro em log.</span><span class="sxs-lookup"><span data-stu-id="cf218-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="cf218-117">Para fazer isso, use o elemento **LogURL** , ESPECIFICANDO uma URL válida para o atributo **href** .</span><span class="sxs-lookup"><span data-stu-id="cf218-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="cf218-118">Você pode incluir elementos **LogURL** como filhos do elemento **ASX** e como filhos de elementos de **entrada** individuais.</span><span class="sxs-lookup"><span data-stu-id="cf218-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="cf218-119">Quando a playlist é aberta pela primeira vez, as informações de log são enviadas para o servidor de origem e para cada URL especificada em **LogURL** filhos do elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="cf218-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="cf218-120">Em seguida, à medida que cada entrada é atingida, as informações de log específicas para essa entrada são enviadas para cada URL especificada em **LogURL** filhos do elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="cf218-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="cf218-121">O SDK do Windows Media Format dá suporte ao elemento **LogURL** por meio da interface **IWMSReaderNetworkConfig** e dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="cf218-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="cf218-122">Além das informações que são registradas automaticamente, uma lista de reprodução de metarquivo pode registrar informações personalizadas por meio do uso do elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="cf218-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="cf218-123">Para usar o elemento **param** dessa forma, defina o atributo **Name** como "log:" seguido de um nome de campo de log e um namespace XML opcional separado do nome do campo por dois pontos (":").</span><span class="sxs-lookup"><span data-stu-id="cf218-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="cf218-124">Tudo depois que o segundo dois pontos é tratado como um namespace, portanto, o nome do campo não deve conter dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="cf218-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="cf218-125">O campo de log especificado no atributo **Name** é definido como o valor do atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="cf218-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="cf218-126">Se o log ainda não contiver um campo com o nome especificado, ele será adicionado.</span><span class="sxs-lookup"><span data-stu-id="cf218-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="cf218-127">**Código de exemplo**</span><span class="sxs-lookup"><span data-stu-id="cf218-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="cf218-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf218-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf218-129">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="cf218-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="cf218-130">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="cf218-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




