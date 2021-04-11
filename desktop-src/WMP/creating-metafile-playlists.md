---
title: Criando listas de reprodução de metarquivo
description: Criando listas de reprodução de metarquivo
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Playlists do metarquivo do Windows Media, criando
- listas de reprodução, criando
- listas de reprodução de metarquivo, criando
- Criando listas de reprodução do metarquivo do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160165"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="8dd0c-107">Criando listas de reprodução de metarquivo</span><span class="sxs-lookup"><span data-stu-id="8dd0c-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="8dd0c-108">Você pode criar uma lista de reprodução usando qualquer editor de texto, como o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="8dd0c-109">Abra seu editor de texto.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-109">Open your text editor.</span></span> <span data-ttu-id="8dd0c-110">Digite as entradas de script que você deseja implementar.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="8dd0c-111">Depois de terminar de digitar no bloco de notas, salve o arquivo com um nome de arquivo e uma extensão de nome de arquivo apropriados.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="8dd0c-112">Para obter mais informações sobre extensões, consulte [diretrizes de extensão de metarquivo](metafile-extension-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="8dd0c-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="8dd0c-113">Normalmente, o nome do arquivo é o nome do arquivo de mídia do Windows ou fluxo seguido por uma extensão de. Wax,. wvx ou. asx.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="8dd0c-114">Por exemplo, se o conteúdo de mídia for um arquivo de áudio do Windows Media que tem uma extensão. WMA, use a extensão. Wax ao nomear a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="8dd0c-115">As listas de reprodução não devem incluir códigos de formatação de um processador de texto, como o Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="8dd0c-116">Para ter certeza de que nenhum código de formatação está incluído na lista de reprodução, salve o arquivo como um arquivo de texto sem formatação ou ASCII.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="8dd0c-117">Elementos e atributos não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="8dd0c-118">O texto usado na lista de reprodução para definir um elemento ou atributo pode ser maiúsculo ou minúsculo, ou uma mistura de ambos.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="8dd0c-119">Se um elemento não tiver elementos filho (aqueles que modificam ou estiverem contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura, logo antes de ' > ', no lugar de uma marca de fechamento.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="8dd0c-120">Os elementos filho de um elemento devem aparecer entre a marca de abertura e de fechamento para esse elemento; caso contrário, eles não são elementos filho para esse elemento e são ignorados ou causam um erro na sintaxe da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="8dd0c-121">Os primeiros quatro caracteres de uma lista de reprodução devem ser " &lt; ASX".</span><span class="sxs-lookup"><span data-stu-id="8dd0c-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="8dd0c-122">O elemento **ASX** é usado em todas as listas de reprodução se sua extensão é. Wax,. wvx ou. asx.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="8dd0c-123">Deve haver apenas um elemento **ASX** por playlist.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="8dd0c-124">Esse elemento identifica o arquivo como uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="8dd0c-125">Ele não especifica o tipo de lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="8dd0c-126">O elemento **ASX** tem três atributos possíveis:</span><span class="sxs-lookup"><span data-stu-id="8dd0c-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="8dd0c-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-127">**VERSION**</span></span>

<span data-ttu-id="8dd0c-128">O atributo **version** é necessário e deve seguir imediatamente após o elemento **ASX** , por exemplo "<ASX Version =" 3,0 " &gt; ".</span><span class="sxs-lookup"><span data-stu-id="8dd0c-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="8dd0c-129">O número da versão atual é 3,0.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-129">The current version number is 3.0.</span></span> <span data-ttu-id="8dd0c-130">O Windows Media Player dá suporte a todas as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="8dd0c-131">Os valores aceitáveis para o atributo **version** incluem 3,0 e 3 (sem ponto decimal).</span><span class="sxs-lookup"><span data-stu-id="8dd0c-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="8dd0c-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="8dd0c-133">O atributo **PREviewmode** é opcional.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="8dd0c-134">Ele fornece outro mecanismo para especificar por quanto tempo renderizar um clipe.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="8dd0c-135">Se o valor do atributo **PREviewmode** for sim, o Windows Media Player processará cada clipe pela duração especificada pelo elemento **PREVIEWDURATION**.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="8dd0c-136">Cada clipe pode ter um **PREVIEWDURATION** especificado.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="8dd0c-137">**BANNERBAR**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-137">**BANNERBAR**</span></span>

<span data-ttu-id="8dd0c-138">O atributo opcional **BANNERBAR** define se o controle do Windows Media Player reserva espaço para um gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="8dd0c-139">(Use o elemento **banner** para especificar o gráfico a ser exibido.) Se o valor de **BANNERBAR** for corrigido, o Windows Media Player reserva espaço em faixa para a apresentação e para cada clipe, independentemente de a lista de reprodução do metarquivo especificar uma faixa para a exibição ou o clipe.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="8dd0c-140">Isso manterá o tamanho da janela do Windows Media Player o mesmo (exceto quando o tamanho do vídeo for alterado), independentemente da ausência ou presença de um gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="8dd0c-141">Se a exibição ou o clipe não tiver uma faixa associada a ele, o espaço reservado para um será preto.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="8dd0c-142">Se o valor do atributo **BANNERBAR** for auto, o Windows Media Player reserva espaço para a faixa somente quando a apresentação ou o clipe inclui um.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="8dd0c-143">Para obter mais informações sobre os três atributos do elemento **ASX** , consulte a entrada de referência para o [elemento ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="8dd0c-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="8dd0c-144">Um elemento **ASX** contém elementos filho de **entrada** que definem informações sobre os arquivos de mídia a serem acessados.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="8dd0c-145">Cada elemento de **entrada** deve conter um elemento **ref** que especifica o caminho para o arquivo de mídia a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="8dd0c-146">Deve haver pelo menos um elemento de **entrada** ou **ENTRYREF** dentro de um elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="8dd0c-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="8dd0c-147">Outros elementos definidos no escopo do elemento **ASX** , como **título** e **autor**, são associados aos metadados exibidos pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="8dd0c-148">As listas de reprodução mais simples são criadas adicionando-se vários elementos de **entrada** com um único elemento **ref** a um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="8dd0c-149">Cada elemento de **entrada** em uma lista de reprodução de metarquivo é renderizado na ordem em que aparece no arquivo, como se o usuário tivesse aberto manualmente cada clipe.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="8dd0c-150">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="8dd0c-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="8dd0c-151">Certifique-se de que a lista de reprodução está funcionando clicando duas vezes nela no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="8dd0c-152">O Windows Media Player deve abrir e iniciar o streaming do conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="8dd0c-153">Depois de confirmar que a lista de reprodução funciona, salve-a em seu servidor Web junto com as páginas da Webe vincule-o por meio de um elemento **href** ou incorpore-o em uma página da Web usando o elemento de **objeto** do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8dd0c-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="8dd0c-154">As seções a seguir contêm mais informações:</span><span class="sxs-lookup"><span data-stu-id="8dd0c-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="8dd0c-155">Aninhando metaarquivos</span><span class="sxs-lookup"><span data-stu-id="8dd0c-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="8dd0c-156">Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="8dd0c-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="8dd0c-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dd0c-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dd0c-158">**Elemento BANNER**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="8dd0c-159">**Exemplos de playlist**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="8dd0c-160">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8dd0c-161">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8dd0c-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




