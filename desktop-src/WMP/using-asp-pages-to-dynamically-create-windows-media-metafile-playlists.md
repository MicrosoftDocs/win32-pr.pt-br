---
title: Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media
description: Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Playlists do metarquivo do Windows Media, criando
- listas de reprodução de metarquivo, criando
- listas de reprodução, criando
- Playlists do metarquivo do Windows Media, criando dinamicamente
- listas de reprodução de metarquivo, criando dinamicamente
- listas de reprodução, criando dinamicamente
- Playlists do metarquivo do Windows Media, páginas ASP
- listas de reprodução de metarquivo, páginas ASP
- listas de reprodução, páginas ASP
- Criando listas de reprodução do metarquivo do Windows Media
- Criando dinamicamente playlists de metarquivo do Windows Media
- Páginas ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498677"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="58edb-115">Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="58edb-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="58edb-116">Você pode usar Active Server páginas (arquivos ASP ou. asp) para gerar listas de reprodução dinamicamente com base nas informações fornecidas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="58edb-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="58edb-117">Uma página ASP é uma página da Web dinâmica usada em conjunto com o Microsoft Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="58edb-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="58edb-118">O ASP é um ambiente no qual você pode combinar HTML, scripts e componentes de servidor ActiveX reutilizáveis para criar soluções de negócios baseadas na Web, dinâmicas e poderosas.</span><span class="sxs-lookup"><span data-stu-id="58edb-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="58edb-119">As páginas ASP permitem o script do lado do servidor para o IIS com suporte nativo para o Microsoft Visual Basic Scripting Edition (VBScript) e o Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="58edb-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="58edb-120">Essa discussão pressupõe que você esteja familiarizado com o ASP e Definindo variáveis.</span><span class="sxs-lookup"><span data-stu-id="58edb-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="58edb-121">Todas as informações de cabeçalho devem estar contidas na primeira linha da cadeia de caracteres da página ASP retornada ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="58edb-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="58edb-122">Ao usar páginas ASP para gerar listas de reprodução, você deve especificar valores para o **ContentType** do objeto de **resposta** e **expirar** as propriedades na página ASP devido a problemas de latência com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="58edb-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="58edb-123">O valor **Response. ContentType** deve ser uma extensão de nome de arquivo válida para os metaarquivos do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="58edb-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="58edb-124">Os valores aceitáveis incluem WMA, Wax, WMV, WVX, ASF e ASX.</span><span class="sxs-lookup"><span data-stu-id="58edb-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="58edb-125">A propriedade **Response. Expires** especifica o período de tempo, em segundos, que o Windows Media Player armazena em cache o arquivo de lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="58edb-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="58edb-126">Especificar um valor de zero resulta no Windows Media Player solicitando uma nova lista de reprodução a partir do servidor sempre que o usuário atualizar a página.</span><span class="sxs-lookup"><span data-stu-id="58edb-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="58edb-127">Consulte o SDK da plataforma para obter detalhes sobre como usar o objeto de **resposta** em páginas Active Server.</span><span class="sxs-lookup"><span data-stu-id="58edb-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="58edb-128">O código a seguir é um exemplo de uma página ASP usada para gerar uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="58edb-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="58edb-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58edb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58edb-130">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="58edb-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




