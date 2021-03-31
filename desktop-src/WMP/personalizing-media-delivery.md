---
title: Personalizando a entrega de mídia
description: Personalizando a entrega de mídia
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Playlists do metarquivo do Windows Media, personalizando a entrega de mídia
- listas de reprodução, personalizando a entrega de mídia
- listas de reprodução de metarquivo, personalizando a entrega de mídia
- Playlists do metarquivo do Windows Media, personalização de entrega de mídia
- listas de reprodução, personalização de entrega de mídia
- listas de reprodução de metarquivo, personalização de entrega de mídia
- personalização de entrega de mídia
- Personalizando a entrega de mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159401"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="3ea7f-111">Personalizando a entrega de mídia</span><span class="sxs-lookup"><span data-stu-id="3ea7f-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="3ea7f-112">Ao contrário da comunicação unidirecional que transmite conteúdo idêntico a um público em massa, as tecnologias de mídia do Windows fornecem as ferramentas para usar os dados demográficos para individualizar as difusões.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="3ea7f-113">Com a Internet, a comunicação bidirecional em grande escala está prontamente disponível.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="3ea7f-114">Esse intercâmbio dinâmico de informações permite que os provedores de conteúdo saibam seu público e respondam com apresentações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="3ea7f-115">O exemplo a seguir, usando uma empresa fictícia, ilustra como a entrega de conteúdo de streaming pode ser personalizada.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="3ea7f-116">Esta discussão pressupõe que você esteja familiarizado com Active Server páginas (arquivos ASP ou. asp) e Definindo variáveis.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="3ea7f-117">A rede de notícias é uma organização de notícias de difusão fictícia que expandiu suas operações para incluir um site.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="3ea7f-118">O principal recurso do site é uma seção em que os usuários podem criar seus próprios newscasts personalizados.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="3ea7f-119">Em vez de exibir um newscast tradicional destinado a um público em massa, um usuário vê um programa de notícias completo que contém apenas tópicos de interesse pessoal.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="3ea7f-120">A sequência a seguir descreve uma experiência de usuário típica.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="3ea7f-121">Um novo usuário vai para o site e clica em **criar seu newscast pessoal**.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="3ea7f-122">Um formulário de preferência é aberto.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-122">A preference form opens.</span></span> <span data-ttu-id="3ea7f-123">Neste formulário, o usuário responde às perguntas sobre as preferências pessoais, como histórias de notícias favoritas, menos histórias de notícias favoritas, Hobbies e o método habitual de receber notícias diárias.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="3ea7f-124">O usuário envia essas informações e alguns segundos depois exibe um newscast pessoal completo, de 15 minutos, que contém o conteúdo do programa, as transições e os negócios.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="3ea7f-125">A seleção de cada elemento de mídia, incluindo os comerciais, é baseada no perfil do usuário e é realizada automaticamente com os componentes das tecnologias de mídia do Windows e as ferramentas de Internet prontas.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="3ea7f-126">A lista a seguir descreve como as várias ferramentas interagem para criar um newscast personalizado.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="3ea7f-127">O formulário de preferência que o usuário preenche é uma página de Active Server (ASP) (Choices. asp).</span><span class="sxs-lookup"><span data-stu-id="3ea7f-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="3ea7f-128">Os dados obtidos do formulário de preferência são analisados por dois componentes de servidor.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="3ea7f-129">Um componente usa as informações para consultar um banco de dados Microsoft SQL Server de histórias de notícias.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="3ea7f-130">O outro componente é um servidor do AD que usa um conjunto complexo de regras com base em requisitos contratuais e demográficos para agendar anúncios apropriados para o usuário naquele momento.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="3ea7f-131">Os dois bancos de dados retornam partes diferentes de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="3ea7f-132">O banco de dados de história de notícias retorna um conjunto de entradas da história apropriadas e o servidor do AD retorna um conjunto de entradas comerciais apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="3ea7f-133">Uma segunda página ASP (PlayShow. asp) recebe as entradas do banco de dados da história de notícias e do servidor do AD e combina aquelas com entradas padrão de exibição abrir, fechar e de transição.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="3ea7f-134">Em seguida, todas as entradas são dispostas de acordo com o modelo fornecido pelo PlayShow. asp, e a página ASP retorna uma lista de reprodução para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="3ea7f-135">O controle do Windows Media Player inserido no computador do usuário reproduz a lista de reprodução do início ao fim e o usuário exibe um newscast personalizado.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="3ea7f-136">O exemplo a seguir é uma parte de um arquivo de lista de reprodução que um usuário pode receber.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="3ea7f-137">Faixas do AD, links MOREINFO e ABSTRATOs foram adicionados a ele.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="3ea7f-138">Os exemplos de empresas, organizações, produtos, pessoas e eventos aqui descritos são fictícios.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="3ea7f-139">Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional nem deve ser presumida.</span><span class="sxs-lookup"><span data-stu-id="3ea7f-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ea7f-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ea7f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea7f-141">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="3ea7f-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3ea7f-142">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="3ea7f-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3ea7f-143">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="3ea7f-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3ea7f-144">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3ea7f-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3ea7f-145">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3ea7f-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




