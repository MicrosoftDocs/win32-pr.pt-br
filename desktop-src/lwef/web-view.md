---
title: Personalizando a exibição da Web de uma pasta
description: Uma exibição da Web é uma maneira poderosa e flexível de usar o Windows Explorer para exibir informações sobre o conteúdo de uma pasta do Shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Exibições da Web
- Estilo clássico
- Estilo da Web
- faixas
- Região de FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640448"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="6f080-108">Personalizando a exibição da Web de uma pasta</span><span class="sxs-lookup"><span data-stu-id="6f080-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="6f080-109">\[Esse recurso tem suporte apenas no Windows XP ou anterior.</span><span class="sxs-lookup"><span data-stu-id="6f080-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="6f080-110">\]</span><span class="sxs-lookup"><span data-stu-id="6f080-110">\]</span></span>

<span data-ttu-id="6f080-111">Uma exibição da Web é uma maneira poderosa e flexível de usar o Windows Explorer para exibir informações sobre o conteúdo de uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="6f080-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="6f080-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="6f080-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="6f080-113">Usando o modelo de exibição da Web</span><span class="sxs-lookup"><span data-stu-id="6f080-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="6f080-114">O corpo do modelo</span><span class="sxs-lookup"><span data-stu-id="6f080-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="6f080-115">O cabeçalho do modelo</span><span class="sxs-lookup"><span data-stu-id="6f080-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="6f080-116">Resumo</span><span class="sxs-lookup"><span data-stu-id="6f080-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="6f080-117">Introdução</span><span class="sxs-lookup"><span data-stu-id="6f080-117">Introduction</span></span>

<span data-ttu-id="6f080-118">O Windows oferece aos usuários duas maneiras principais de exibir e navegar no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="6f080-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="6f080-119">A mais familiar delas, o estilo clássico, é semelhante ao familiar Gerenciador de arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="6f080-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="6f080-120">O painel direito lista o conteúdo da pasta selecionada no momento em um dos cinco formatos: ícone grande, ícone pequeno, lista, detalhes e miniatura.</span><span class="sxs-lookup"><span data-stu-id="6f080-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="6f080-121">A principal diferença do Gerenciador de arquivos do Windows é o painel esquerdo, que parece muito semelhante à barra do Explorer do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6f080-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="6f080-122">Ele pode ser redimensionado ou removido e pode exibir vários painéis, além da conhecida árvore do sistema de arquivos, como um painel de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6f080-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="6f080-123">As informações neste documento não se aplicam ao Windows XP, as técnicas discutidas se aplicam somente a versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="6f080-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="6f080-124">A ilustração a seguir mostra a pasta impressoras no estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-124">The following illustration shows the Printers folder in Classic style.</span></span>

![estilo clássico da pasta impressoras.](images/webview1.png)

<span data-ttu-id="6f080-126">O estilo clássico funciona razoavelmente bem para arquivos e pastas do sistema de arquivos normais.</span><span class="sxs-lookup"><span data-stu-id="6f080-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="6f080-127">No entanto, com a introdução do Windows 95, o sistema de arquivos evoluiu para o namespace.</span><span class="sxs-lookup"><span data-stu-id="6f080-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="6f080-128">O namespace permite a criação de *pastas virtuais*, como impressoras ou ambiente de rede, que podem representar tipos muito diferentes de informações do que uma pasta normal do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6f080-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="6f080-129">O estilo da Web, também conhecido como exibição da Web, oferece uma maneira mais flexível e eficiente de apresentar informações do que o estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="6f080-130">Em uma exibição da Web, o usuário basicamente exibe e navega o namespace usando o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6f080-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="6f080-131">O layout básico de uma exibição da Web é semelhante ao estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="6f080-132">A barra do Gerenciador não foi alterada.</span><span class="sxs-lookup"><span data-stu-id="6f080-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="6f080-133">No entanto, a região ocupada pela lista de arquivos se torna uma área de exibição de uso geral que é efetivamente uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="6f080-134">Uma exibição da Web ainda é usada para exibir informações sobre o conteúdo de uma pasta, mas há algumas restrições sobre quais informações são exibidas ou como.</span><span class="sxs-lookup"><span data-stu-id="6f080-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="6f080-135">Cada pasta pode ter sua própria exibição da Web, personalizada para se adequar a seus recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="6f080-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="6f080-136">A ilustração a seguir mostra uma exibição da Web da pasta impressoras (mostrada anteriormente no estilo clássico).</span><span class="sxs-lookup"><span data-stu-id="6f080-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![exibição da Web padrão da pasta impressoras.](images/webview2.png)

<span data-ttu-id="6f080-138">Da mesma forma que as páginas da Web convencionais, as exibições são controladas por um modelo baseado em HTML.</span><span class="sxs-lookup"><span data-stu-id="6f080-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="6f080-139">A criação de um modelo de exibição da Web é quase idêntica à criação de uma página da Web e fornece o mesmo grau de flexibilidade no conteúdo e no layout das informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="6f080-140">Os modelos de exibição da Web podem usar HTML dinâmico (DHTML) e scripts para responder a eventos, como um usuário clicando em um item.</span><span class="sxs-lookup"><span data-stu-id="6f080-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="6f080-141">Eles também podem hospedar objetos que permitem obter e exibir informações da pasta ou seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6f080-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="6f080-142">O usuário pode escolher uma exibição da Web iniciando o Windows Explorer, clicando em **Opções de pasta** no menu **Exibir** e selecionando esta opção: **habilitar o conteúdo da Web em pastas**.</span><span class="sxs-lookup"><span data-stu-id="6f080-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="6f080-143">No entanto, o usuário também pode iniciar o Internet Explorer e apontar o navegador no sistema de arquivos clicando no menu **Exibir** , apontando para a **barra do Explorer** e clicando em **pastas**.</span><span class="sxs-lookup"><span data-stu-id="6f080-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="6f080-144">Em uma exibição da Web, praticamente não há nenhuma diferença entre o Internet Explorer e o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6f080-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="6f080-145">No lado esquerdo do painel direito, a exibição da Web impressoras exibe uma faixa com o nome e o ícone da pasta, seguido por um bloco de informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="6f080-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="6f080-146">A lista de arquivos usual ocupa o lado direito da página.</span><span class="sxs-lookup"><span data-stu-id="6f080-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="6f080-147">Quando um usuário clica em um item, informações detalhadas sobre o item são exibidas no bloco de informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="6f080-148">Na verdade, a exibição da Web de impressoras exibe muitas das mesmas informações disponíveis no estilo clássico, mas faz isso em um formato mais utilizável.</span><span class="sxs-lookup"><span data-stu-id="6f080-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="6f080-149">No entanto, uma exibição da Web não é simplesmente uma maneira diferente de exibir informações de estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="6f080-150">Por exemplo, um link para um site útil pode ser exibido abaixo do bloco de informações, um recurso que não está disponível no estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="6f080-151">Se o usuário clicar no link, o site será exibido.</span><span class="sxs-lookup"><span data-stu-id="6f080-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="6f080-152">A exibição da Web de impressoras mostrada na ilustração anterior é semelhante ao estilo clássico, pois o modelo de exibição da Web subjacente (um arquivo. htt) foi escrito dessa forma.</span><span class="sxs-lookup"><span data-stu-id="6f080-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="6f080-153">A lista de arquivos, por exemplo, não é gerada diretamente pelo modelo de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="6f080-154">Ele é criado e exibido por um objeto [**WebViewFolderContents**](webviewfoldercontents.md) hospedado pelo modelo de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="6f080-155">Os métodos e as propriedades do objeto permitem que o modo de exibição da Web controle seu layout e obtenha informações sobre itens específicos.</span><span class="sxs-lookup"><span data-stu-id="6f080-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="6f080-156">O conteúdo e o layout da faixa e do bloco de informações são especificados no modelo de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="6f080-157">Como uma exibição da Web dá suporte a DHTML, o modelo também pode ser usado para lidar com a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f080-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="6f080-158">Por exemplo, quando um usuário clica em um dos ícones da impressora, o objeto **WebViewFolderIcon** dispara um evento [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) .</span><span class="sxs-lookup"><span data-stu-id="6f080-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="6f080-159">O modelo usa um manipulador de eventos DHTML escrito em script para recuperar as informações solicitadas e exibi-las no bloco de informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="6f080-160">Esse exemplo simples para a pasta impressoras não é o único modo de usar uma exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="6f080-161">Ao escrever seu próprio modelo e, se necessário, objetos, você pode usar uma exibição da Web para exibir informações e interagir com o usuário da mesma maneira que achar mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="6f080-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="6f080-162">Observe que, no momento, os modelos de exibição da Web só exibem pastas virtuais definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6f080-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="6f080-163">Embora os desenvolvedores possam criar uma pasta virtual implementando uma extensão de namespace, eles devem usar as técnicas descritas em [extensões de namespace](/windows/desktop/shell/nse-works) para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="6f080-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="6f080-164">Usando o modelo de exibição da Web</span><span class="sxs-lookup"><span data-stu-id="6f080-164">Using the Web View Template</span></span>

<span data-ttu-id="6f080-165">A maneira como os dados são exibidos em uma exibição da Web pode ser personalizada de forma limitada, modificando o arquivo de Desktop.ini de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6f080-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="6f080-166">Consulte [Personalizando pastas com Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6f080-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="6f080-167">Uma maneira muito mais flexível e eficiente de personalizar uma exibição da Web é criar um modelo de exibição da Web personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f080-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="6f080-168">O modelo de exibição da Web controla o que é exibido em uma exibição da Web e como.</span><span class="sxs-lookup"><span data-stu-id="6f080-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="6f080-169">Ele usa as técnicas de HTML, DHTML e script padrão para obter e exibir informações e interagir com o usuário.</span><span class="sxs-lookup"><span data-stu-id="6f080-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="6f080-170">Esta seção discute como criar um modo de exibição da Web examinando um modelo simples – Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="6f080-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



<span data-ttu-id="6f080-171">Uma maneira simples de criar seu próprio modelo de exibição da Web é usar o Generic. htt e modificá-lo.</span><span class="sxs-lookup"><span data-stu-id="6f080-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="6f080-172">Como é bastante limitado, você também deve examinar outros exemplos mais complexos de ideias adicionais.</span><span class="sxs-lookup"><span data-stu-id="6f080-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="6f080-173">Você pode encontrá-los pesquisando o sistema para a extensão. htt usada por todos os modelos de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="6f080-174">Se você quiser criar um modelo personalizado para uma pasta, inicie com o modelo Folder. htt padrão, que geralmente é armazenado em C: \\ WinNT \\ Web ou c: \\ Windows \\ Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="6f080-175">Observe que esses arquivos são definidos como ocultos, portanto, talvez seja necessário modificar as configurações do Windows Explorer para exibi-los.</span><span class="sxs-lookup"><span data-stu-id="6f080-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="6f080-176">Quando um arquivo. htt é criado, ele deve ser marcado como somente leitura e oculto.</span><span class="sxs-lookup"><span data-stu-id="6f080-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="6f080-177">Os modelos de exibição da Web usam a extensão. htt porque diferem ligeiramente dos documentos. htm convencionais.</span><span class="sxs-lookup"><span data-stu-id="6f080-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="6f080-178">A principal diferença é várias variáveis especiais em arquivos. htt que o sistema substitui pelos valores atuais do namespace.</span><span class="sxs-lookup"><span data-stu-id="6f080-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="6f080-179">As variáveis% THISDIR% e% THISDIRPATH% representam o nome e o caminho da pasta selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="6f080-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="6f080-180">A variável% TEMPLATEDIR% representa a pasta onde as folhas de estilo de exibição da Web são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="6f080-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="6f080-181">Assim como a maioria dos modelos HTML, os arquivos. htt têm duas partes básicas: um corpo e um cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6f080-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="6f080-182">O corpo do modelo controla o layout básico da exibição da Web e carrega os objetos usados para se comunicar com o namespace e informações de exibição.</span><span class="sxs-lookup"><span data-stu-id="6f080-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="6f080-183">O cabeçalho contém scripts e funções que fazem tarefas como a manipulação de redimensionamento e obtenção de informações da pasta.</span><span class="sxs-lookup"><span data-stu-id="6f080-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="6f080-184">A maioria dos modelos, incluindo Generic. htt, também inclui uma folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="6f080-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="6f080-185">Em geral, é melhor incluir as informações da folha de estilo em seu modelo.</span><span class="sxs-lookup"><span data-stu-id="6f080-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="6f080-186">Folhas de estilo separadas podem não funcionar corretamente quando uma exibição da Web é usada com namespaces remotos.</span><span class="sxs-lookup"><span data-stu-id="6f080-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="6f080-187">O corpo do modelo</span><span class="sxs-lookup"><span data-stu-id="6f080-187">The Template Body</span></span>

<span data-ttu-id="6f080-188">O corpo do modelo especifica o que será apresentado por uma exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="6f080-189">Também é onde os objetos usados para exibir informações e se comunicar com pastas de namespace são carregados.</span><span class="sxs-lookup"><span data-stu-id="6f080-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="6f080-190">O layout definido por Generic. htt é semelhante ao mostrado na ilustração da seção anterior.</span><span class="sxs-lookup"><span data-stu-id="6f080-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="6f080-191">Há três regiões de exibição: a faixa e o bloco de informações no lado esquerdo da exibição e a lista de arquivos à direita.</span><span class="sxs-lookup"><span data-stu-id="6f080-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="6f080-192">As regiões são todos os identificadores atribuídos a serem usados pela folha de estilos e por DHTML.</span><span class="sxs-lookup"><span data-stu-id="6f080-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="6f080-193">Conforme discutido na próxima seção, há duas faixas possíveis, com identificadores de "faixa" e "MiniBanner".</span><span class="sxs-lookup"><span data-stu-id="6f080-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="6f080-194">O identificador da região do bloco de informações é "info".</span><span class="sxs-lookup"><span data-stu-id="6f080-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="6f080-195">O identificador do objeto de lista de arquivos é "FileList".</span><span class="sxs-lookup"><span data-stu-id="6f080-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="6f080-196">Os detalhes do [layout](#controlling-the-web-view-layout) da região são tratados pela folha de estilos e uma função do Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), que é abordada posteriormente no capítulo.</span><span class="sxs-lookup"><span data-stu-id="6f080-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="6f080-197">A região de faixa</span><span class="sxs-lookup"><span data-stu-id="6f080-197">The Banner Region</span></span>

<span data-ttu-id="6f080-198">A faixa está localizada na parte superior da exibição, no canto superior esquerdo da exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="6f080-199">A faixa normal exibe o nome e o ícone da pasta cujos conteúdos são exibidos na lista de arquivos à direita.</span><span class="sxs-lookup"><span data-stu-id="6f080-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="6f080-200">No entanto, se a janela se tornar muito curta, pode não haver espaço abaixo do ícone para exibir informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="6f080-201">Por esse motivo, Generic. htt também define um minibanner que exibe apenas o nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="6f080-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="6f080-202">As duas faixas são inicialmente definidas como ocultas.</span><span class="sxs-lookup"><span data-stu-id="6f080-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="6f080-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) escolhe qual deles deve ser exibido e o define como "Visible".</span><span class="sxs-lookup"><span data-stu-id="6f080-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="6f080-204">A faixa normal para Generic. htt é definida por:</span><span class="sxs-lookup"><span data-stu-id="6f080-204">The normal banner for Generic.htt is defined by:</span></span>


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



<span data-ttu-id="6f080-205">A primeira parte da seção de faixa exibe o título com uma regra horizontal abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="6f080-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="6f080-206">Marcas de tabela são usadas para controlar sua posição.</span><span class="sxs-lookup"><span data-stu-id="6f080-206">Table tags are used to control its position.</span></span> <span data-ttu-id="6f080-207">O atributo nowrap está definido para o</span><span class="sxs-lookup"><span data-stu-id="6f080-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="6f080-208">marca para evitar quebra automática de texto.</span><span class="sxs-lookup"><span data-stu-id="6f080-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="6f080-209">O sistema substituirá% THISDIRNAME% pelo nome da pasta atual.</span><span class="sxs-lookup"><span data-stu-id="6f080-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="6f080-210">Um objeto **WebViewFolderIcon** , com um identificador de "Icon" para simplificar, é então carregado para extrair e exibir o ícone da pasta.</span><span class="sxs-lookup"><span data-stu-id="6f080-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="6f080-211">A seção minibanner é semelhante à faixa normal.</span><span class="sxs-lookup"><span data-stu-id="6f080-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="6f080-212">O formato do título é colocado ligeiramente mais alto e não tem uma regra.</span><span class="sxs-lookup"><span data-stu-id="6f080-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="6f080-213">Como não há nenhum ícone, o objeto **WebViewFolderIcon** não é carregado.</span><span class="sxs-lookup"><span data-stu-id="6f080-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="6f080-214">A região de informações</span><span class="sxs-lookup"><span data-stu-id="6f080-214">The Info Region</span></span>

<span data-ttu-id="6f080-215">A parte da exibição da Web abaixo da faixa é usada para apresentar informações detalhadas sobre o item selecionado.</span><span class="sxs-lookup"><span data-stu-id="6f080-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="6f080-216">Se nenhum item for selecionado, uma mensagem padrão será mostrada.</span><span class="sxs-lookup"><span data-stu-id="6f080-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="6f080-217">Como Generic. htt exibe apenas um único bloco de texto, esta seção é bem simples.</span><span class="sxs-lookup"><span data-stu-id="6f080-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="6f080-218">A maior parte do trabalho de coletar as informações é tratada por um [script de informações de pasta](#retrieving-and-displaying-folder-information) que é discutido posteriormente neste capítulo.</span><span class="sxs-lookup"><span data-stu-id="6f080-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="6f080-219">Ele exibe as informações atribuindo o texto a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6f080-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="6f080-220">Você pode personalizar facilmente a exibição das informações modificando esses elementos ou incluindo outros.</span><span class="sxs-lookup"><span data-stu-id="6f080-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="6f080-221">Qualquer coisa que você possa colocar em uma página da Web pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f080-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="6f080-222">Por exemplo, para exibir um link para seu site, você pode adicionar um elemento de âncora após o bloco de texto em Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="6f080-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a><span data-ttu-id="6f080-223">A região de FileList</span><span class="sxs-lookup"><span data-stu-id="6f080-223">The FileList Region</span></span>

<span data-ttu-id="6f080-224">Finalmente, Generic. htt carrega um objeto [**WebViewFolderContents**](webviewfoldercontents.md) para a região FileList.</span><span class="sxs-lookup"><span data-stu-id="6f080-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="6f080-225">Como seu identificador está definido como "FileList", ele será referido como o objeto FileList de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="6f080-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="6f080-226">O objeto FileList é encontrado na maioria dos modos de exibição da Web e atende a várias finalidades.</span><span class="sxs-lookup"><span data-stu-id="6f080-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="6f080-227">FileList exibe a lista de itens contidos na pasta selecionada com as mesmas opções e aparência que a lista de arquivos no estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="6f080-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="6f080-228">Quando um item é selecionado, o FileList notifica a exibição da Web acionando um evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="6f080-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="6f080-229">O FileList também expõe métodos e propriedades que podem ser usados para recuperar informações sobre itens individuais e controlar a posição e o tamanho de sua área de exibição.</span><span class="sxs-lookup"><span data-stu-id="6f080-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="6f080-230">Embora o objeto FileList seja muito útil, ele retorna apenas informações padrão do sistema de arquivos, como o tamanho do arquivo ou os atributos.</span><span class="sxs-lookup"><span data-stu-id="6f080-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="6f080-231">Para recuperar outros tipos de informações de uma pasta do Shell, você precisará carregar e manipular objetos adicionais.</span><span class="sxs-lookup"><span data-stu-id="6f080-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="6f080-232">Qualquer objeto que possa ser hospedado por uma página da Web pode ser usado com um modo de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="6f080-233">O cabeçalho do modelo</span><span class="sxs-lookup"><span data-stu-id="6f080-233">The Template Head</span></span>

<span data-ttu-id="6f080-234">O cabeçalho do modelo de exibição da Web contém os scripts e funções que fazem a maior parte do trabalho real.</span><span class="sxs-lookup"><span data-stu-id="6f080-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="6f080-235">Há duas tarefas essenciais que precisam ser tratadas.</span><span class="sxs-lookup"><span data-stu-id="6f080-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="6f080-236">Um é o layout do modo de exibição da Web, que precisa ser ajustado para acomodar diferentes regiões de exibição.</span><span class="sxs-lookup"><span data-stu-id="6f080-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="6f080-237">A outra é recuperar e exibir informações da pasta quando um item é selecionado.</span><span class="sxs-lookup"><span data-stu-id="6f080-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="6f080-238">Assim como nas folhas de estilo, é melhor incluir todos os scripts e funções no modelo em vez de fazer referência a eles como arquivos separados.</span><span class="sxs-lookup"><span data-stu-id="6f080-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="6f080-239">Controlando o layout da exibição da Web</span><span class="sxs-lookup"><span data-stu-id="6f080-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="6f080-240">A área disponível para uma exibição da Web depende do tamanho da janela de exibição da Web e de quanto ela é exibida pela barra do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6f080-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="6f080-241">Essa área será alterada sempre que a janela ou a barra do Windows Explorer for redimensionada.</span><span class="sxs-lookup"><span data-stu-id="6f080-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="6f080-242">Portanto, o layout precisa ser correspondido à área disponível quando uma exibição da Web é carregada e alterada adequadamente quando é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="6f080-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="6f080-243">Grande parte do layout é especificada na folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="6f080-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="6f080-244">A região de informações, por exemplo, é definida para ocupar os 30% mais à esquerda da exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="6f080-245">Como uma exibição da Web é redimensionada, a largura da região de informações será alterada para manter esse percentual.</span><span class="sxs-lookup"><span data-stu-id="6f080-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="6f080-246">O [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gerencia os problemas de layout que não podem ser manipulados por uma folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="6f080-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="6f080-247">Carregando e inicializando a exibição da Web</span><span class="sxs-lookup"><span data-stu-id="6f080-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="6f080-248">Quando uma exibição da Web é carregada, o layout precisa ser ajustado para se ajustar à área de exibição disponível.</span><span class="sxs-lookup"><span data-stu-id="6f080-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="6f080-249">Como nenhum item foi selecionado ainda, exibições da Web normalmente exibem algumas informações padrão que se aplicam à pasta inteira.</span><span class="sxs-lookup"><span data-stu-id="6f080-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="6f080-250">Para lidar com a inicialização, o</span><span class="sxs-lookup"><span data-stu-id="6f080-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="6f080-251">a marca para Generic. htt detecta o evento [OnLoad](/previous-versions//ms531409(v=vs.85)) e chama a função **init** .</span><span class="sxs-lookup"><span data-stu-id="6f080-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="6f080-252">**Init** é uma função JScript simples.</span><span class="sxs-lookup"><span data-stu-id="6f080-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="6f080-253">**Init** associa [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ao evento [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) para que ele seja chamado sempre que a área de exibição da Web exibir for alterada.</span><span class="sxs-lookup"><span data-stu-id="6f080-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="6f080-254">Em seguida, ele executa FixSize para definir o layout inicial e atribui o \_ texto introdutório de L \_ à região de informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="6f080-255">L \_ \_ texto introdutório é um bloco de texto introdutório que é definido na seção folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="6f080-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="6f080-256">Ajustando o layout usando a função FixSize</span><span class="sxs-lookup"><span data-stu-id="6f080-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="6f080-257">A função [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) é usada para especificar vários aspectos do layout que não podem ser manipulados pela folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="6f080-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="6f080-258">Há duas faixas possíveis que podem ser usadas, dependendo da altura da exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



<span data-ttu-id="6f080-259">Generic. htt usa uma altura de 200 pixels como a linha de divisão entre normal e minibanners.</span><span class="sxs-lookup"><span data-stu-id="6f080-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="6f080-260">Ele define o estilo da faixa selecionada como visível e a outra como oculta.</span><span class="sxs-lookup"><span data-stu-id="6f080-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="6f080-261">Ele também define várias propriedades de layout para as regiões info e FileList para que caibam corretamente com a faixa selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f080-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="6f080-262">Se uma exibição da Web se tornar muito estreita, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usará a largura total da área de exibição para a exibição de FileList.</span><span class="sxs-lookup"><span data-stu-id="6f080-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



<span data-ttu-id="6f080-263">Generic. htt usa 400 pixels como a linha de divisão entre monitores estreitos e largos.</span><span class="sxs-lookup"><span data-stu-id="6f080-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="6f080-264">Se a exibição da Web for muito estreita, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ocultará a região de informações e modificará a propriedade [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) do FileList para que ela preencha toda a região abaixo da faixa.</span><span class="sxs-lookup"><span data-stu-id="6f080-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="6f080-265">As poucas linhas finais de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustam várias propriedades de layout com base nos resultados do código anterior.</span><span class="sxs-lookup"><span data-stu-id="6f080-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="6f080-266">A largura da região de FileList é ajustada para que ela preencha exatamente a parte da exibição da Web não ocupada pela região de informações.</span><span class="sxs-lookup"><span data-stu-id="6f080-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="6f080-267">A altura da região de informações é dimensionada para caber entre a faixa e a parte inferior da exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="6f080-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="6f080-268">Recuperando e exibindo informações da pasta</span><span class="sxs-lookup"><span data-stu-id="6f080-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="6f080-269">Quando um usuário seleciona um item, o objeto FileList dispara um evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="6f080-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="6f080-270">Esse evento é tratado por um script JScript.</span><span class="sxs-lookup"><span data-stu-id="6f080-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="6f080-271">Para simplificar, o script encontrado em Generic. htt pressupõe que apenas um item pode ser selecionado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="6f080-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



<span data-ttu-id="6f080-272">O script usa duas propriedades de FileList, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)e [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) para obter informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="6f080-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="6f080-273">**FileList. FocusedItem** identifica o item selecionado, com o nome do item fornecido por **FileList.FocusedItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="6f080-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="6f080-274">**FileList. Folder** é, na verdade, um ponteiro para um objeto de [**pasta**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="6f080-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="6f080-275">O método [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) do objeto de pasta é usado para recuperar as informações restantes sobre o item.</span><span class="sxs-lookup"><span data-stu-id="6f080-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="6f080-276">Todas as informações são concatenadas em uma única cadeia de texto, separadas por</span><span class="sxs-lookup"><span data-stu-id="6f080-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="6f080-277">marcas para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="6f080-277">tags for readability.</span></span> <span data-ttu-id="6f080-278">Em seguida, o texto é exibido atribuindo-o a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6f080-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="6f080-279">Resumo</span><span class="sxs-lookup"><span data-stu-id="6f080-279">Summary</span></span>

<span data-ttu-id="6f080-280">Este capítulo descreve algumas das técnicas que você pode usar para personalizar a maneira como o Windows Explorer exibe informações sobre pastas do Shell.</span><span class="sxs-lookup"><span data-stu-id="6f080-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="6f080-281">A criação de um arquivo de Desktop.ini permite que você faça uma personalização simples, como exibir um ícone personalizado no lugar do ícone de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="6f080-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="6f080-282">Quando uma pasta é exibida em uma exibição da Web, seu layout e exibição são controlados por um modelo baseado em HTML que determina quais informações são exibidas e como.</span><span class="sxs-lookup"><span data-stu-id="6f080-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="6f080-283">Você pode exercer um alto grau de controle sobre a exibição da Web de uma pasta usando HTML, DHTML e técnicas de script padrão para criar um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f080-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 