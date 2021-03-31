---
title: Usando links relativos em metaarquivos
description: Usando links relativos em metaarquivos
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Playlists do metarquivo do Windows Media, links relativos
- listas de reprodução, links relativos
- listas de reprodução de metarquivo, links relativos
- metaarquivos, links relativos
- Metaarquivos do Windows Media, links relativos
- links relativos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822481"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="5e58e-109">Usando links relativos em metaarquivos</span><span class="sxs-lookup"><span data-stu-id="5e58e-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="5e58e-110">Links relativos são um recurso totalmente suportado de metaarquivos do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5e58e-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="5e58e-111">Você pode usar links relativos em metaarquivos da mesma forma que os usa em documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="5e58e-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="5e58e-112">O uso de links relativos permite criar metarquivos que são portáteis, o que significa que você pode copiar ou mover uma estrutura de diretório inteira para outro servidor sem Atualizar os caminhos para arquivos gráficos usados como faixas ou os atributos **href** de elementos **moreinfo** (se eles fizerem referência a arquivos no mesmo servidor Web que o metarquivo armazenado).</span><span class="sxs-lookup"><span data-stu-id="5e58e-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="5e58e-113">Os links relativos funcionam, em qualquer aplicativo que ofereça suporte a eles, porque as partes da URL não incluídas no atributo **href** de um elemento são incluídas na URL enviada pelo aplicativo para o servidor quando essa URL é solicitada.</span><span class="sxs-lookup"><span data-stu-id="5e58e-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="5e58e-114">Isso significa que o protocolo (como https://), o nome do servidor e o diretório virtual no qual o arquivo que contém o link relativo está localizado são todos incluídos na URL que é enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="5e58e-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="5e58e-115">Se o arquivo de mídia ou URL ao qual você vincular usando um link relativo não residir no mesmo servidor que o metarquivo, o link relativo não será válido.</span><span class="sxs-lookup"><span data-stu-id="5e58e-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="5e58e-116">Essas informações sobre links relativos só estão corretas quando se usa um link para os metaarquivos que são abertos no Windows Media Player autônomo.</span><span class="sxs-lookup"><span data-stu-id="5e58e-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="5e58e-117">Quando você usa o controle incorporado do Windows Media Player, todos os links são relativos à página na qual o controle está hospedado, a menos que o elemento filho **base** do elemento **ASX** seja usado para redirecionar o caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="5e58e-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="5e58e-118">Todos os links relativos no metarquivo devem ser totalmente relativos, não relativos à unidade, para mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="5e58e-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="5e58e-119">Quando uma URL começa com um \\ caractere "", o link é relativo à unidade.</span><span class="sxs-lookup"><span data-stu-id="5e58e-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="5e58e-120">O Windows Media Player tenta abrir o arquivo vinculado ao na unidade em que o metarquivo foi aberto, geralmente um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="5e58e-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="5e58e-121">Como os servidores Web usam diretórios virtuais, o Windows Media Player tenta localizar o fluxo especificado ou o arquivo de mídia em um subdiretório de um diretório virtual no servidor Web onde o metarquivo foi aberto.</span><span class="sxs-lookup"><span data-stu-id="5e58e-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="5e58e-122">Um usuário não teria acesso a um diretório de servidor.</span><span class="sxs-lookup"><span data-stu-id="5e58e-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="5e58e-123">O exemplo nesta seção ilustra o uso de um link totalmente relativo.</span><span class="sxs-lookup"><span data-stu-id="5e58e-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="5e58e-124">Você pode usar links relativos à unidade ao usar metarquivos em um único computador onde todos os arquivos de mídia vinculados à lista de reprodução de metarquivo existem em um dispositivo de armazenamento nesse computador.</span><span class="sxs-lookup"><span data-stu-id="5e58e-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="5e58e-125">No entanto, não é possível transmitir mídia dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="5e58e-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="5e58e-126">Quando você usa um link para outro metarquivo para permitir links relativos, o nome exibido como o título pelo Windows Media Player é o título no metarquivo original.</span><span class="sxs-lookup"><span data-stu-id="5e58e-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="5e58e-127">Links relativos não podem ser usados para URLs para um servidor de mídia de streaming porque diferentes protocolos são usados para acessar conteúdo de streaming de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e58e-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="5e58e-128">Na playlist de exemplo a seguir, o primeiro **ENTRYREF** contém uma URL para outra playlist, relativa. Wax.</span><span class="sxs-lookup"><span data-stu-id="5e58e-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="5e58e-129">O exemplo a seguir é o arquivo Relative. Wax, que contém links relativos.</span><span class="sxs-lookup"><span data-stu-id="5e58e-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="5e58e-130">A URL que contém a referência à playlist, relativa. Wax, pode existir em uma lista de reprodução de metarquivo em qualquer lugar que possa ser acessada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e58e-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="5e58e-131">Para que a URL seja processada com êxito, deve haver um servidor Web chamado "example.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="5e58e-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="5e58e-132">Esse servidor Web deve ter um diretório virtual definido como "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="5e58e-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="5e58e-133">A lista de reprodução referenciada, relativa. Wax, deve existir no servidor Web chamado "example.microsoft.com" no diretório virtual "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="5e58e-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="5e58e-134">Para os arquivos de mídia referenciados na playlist relativa. Wax a ser acessado e reproduzido com êxito, deve haver um diretório chamado "Graphics", que é um subdiretório do "Metafiles" do diretório virtual do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e58e-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="5e58e-135">O arquivo de gráficos Logo1.jpg, referenciado no elemento **banner** , deve ser o subdiretório chamado Graphics.</span><span class="sxs-lookup"><span data-stu-id="5e58e-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="5e58e-136">Da mesma forma, um documento chamado Category1.htm deve residir em um subdiretório chamado Category1.</span><span class="sxs-lookup"><span data-stu-id="5e58e-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="5e58e-137">O diretório chamado Category1 deve existir como um subdiretório dos "metaarquivos" do diretório virtual no servidor Web example.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5e58e-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e58e-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e58e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e58e-139">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="5e58e-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5e58e-140">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="5e58e-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5e58e-141">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5e58e-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5e58e-142">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5e58e-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




