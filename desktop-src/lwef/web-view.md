---
title: Personalização da exibição da Web de uma pasta
description: Uma exibição da Web é uma maneira poderosa e flexível de usar o Windows Explorer para exibir informações sobre o conteúdo de uma pasta shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Exibições da Web
- Estilo clássico
- Estilo da Web
- faixas
- Região FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ebe106bdada4da55eef8891a3c93ee82aba3cc4da9194e1fcd4c7e71bcd4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745673"
---
# <a name="customizing-a-folders-web-view"></a>Personalização da exibição da Web de uma pasta

\[Esse recurso só tem suporte no Windows XP ou anterior. \]

Uma exibição da Web é uma maneira poderosa e flexível de usar o Windows Explorer para exibir informações sobre o conteúdo de uma pasta shell.

-   [Introdução](#introduction)
-   [Usando o modelo de exibição da Web](#using-the-web-view-template)
    -   [O corpo do modelo](#the-template-body)
    -   [O cabeça do modelo](#the-template-head)
-   [Resumo](#summary)

## <a name="introduction"></a>Introdução

Windows oferece aos usuários duas maneiras principais de exibir e navegar pelo namespace shell. O mais familiar deles, o estilo Clássico, é semelhante ao gerenciador de arquivos Windows familiar. O painel direito lista o conteúdo da pasta selecionada no momento em um dos cinco formatos: Ícone Grande, Ícone Pequeno, Lista, Detalhes e Miniatura. A principal diferença do Windows File Manager é o painel esquerdo, que é muito semelhante à barra explorer do Windows Internet Explorer. Ele pode ser reessado ou removido e pode exibir vários painéis além da árvore familiar do sistema de arquivos, como um painel de pesquisa.

> [!Note]  
> As informações neste documento não se aplicam ao Windows XP, as técnicas discutidas se aplicam somente a versões anteriores do Windows.

 

A ilustração a seguir mostra a pasta Impressoras no estilo Clássico.

![estilo clássico da pasta impressoras.](images/webview1.png)

O estilo Clássico funciona razoavelmente bem para arquivos e pastas normais do sistema de arquivos. No entanto, com a introdução Windows 95, o sistema de arquivos evoluiu para o namespace . O namespace permite a criação de pastas virtuais , como *Impressoras* ou Network Neighborhood, que podem representar tipos muito diferentes de informações que uma pasta normal do sistema de arquivos.

O estilo Web, também conhecido como exibição da Web, oferece uma maneira mais flexível e poderosa de apresentar informações do que o estilo Clássico. Em uma exibição da Web, o usuário basicamente visualiza e navega pelo namespace usando Internet Explorer. O layout básico de uma exibição da Web é semelhante ao estilo Clássico. A barra do Explorer permanece inalterada. No entanto, a região ocupada pela lista de arquivos se torna uma área de exibição de uso geral que é efetivamente uma página da Web. Uma exibição da Web ainda é usada para exibir informações sobre o conteúdo de uma pasta, mas há algumas restrições sobre quais informações são exibidas ou como. Cada pasta pode ter sua própria exibição da Web, personalizada para atender a seus recursos específicos.

A ilustração a seguir mostra uma exibição da Web da pasta Impressoras (mostrada anteriormente no estilo Clássico).

![exibição da Web padrão da pasta impressoras.](images/webview2.png)

Assim como as páginas da Web convencionais, as exibições da Web são controladas por um modelo baseado em HTML. A aplicação de um modelo de exibição da Web é quase idêntica à de autor de uma página da Web e fornece o mesmo grau de flexibilidade no conteúdo e no layout das informações. Os modelos de exibição da Web podem usar HTML dinâmico (DHTML) e script para responder a eventos, como um usuário clicando em um item. Eles também podem hospedar objetos que permitem obter e exibir informações da pasta ou seu conteúdo.

O usuário pode escolher um modo de exibição  da Web iniciando Windows Explorer, clicando em Opções de Pasta no **menu** Exibir e selecionando esta opção: Habilitar conteúdo da Web nas **pastas**. No entanto, o usuário também pode iniciar Internet Explorer e apontar o navegador para o sistema de arquivos clicando no **menu** Exibir, apontando para Barra do **Explorer** e clicando **em Pastas**. Em uma exibição da Web, praticamente não há nenhuma diferença entre Internet Explorer e Windows Explorer.

No lado esquerdo do painel direito, a exibição da Web Impressoras exibe uma faixa com o nome e o ícone da pasta, seguidos por um bloco de informações sobre a pasta. A lista de arquivos normal ocupa o lado direito da página.

Quando um usuário clica em um item, informações detalhadas sobre o item são exibidas no bloco de informações. O modo de exibição da Web impressoras, na verdade, exibe muito as mesmas informações que estão disponíveis no estilo Clássico, mas faz isso em um formato mais acessível. No entanto, uma exibição da Web não é simplesmente uma maneira diferente de exibir informações de estilo clássico. Por exemplo, um link para um site útil pode ser exibido abaixo do bloco de informações, um recurso que não está disponível no estilo Clássico. Se o usuário clicar no link, o site será exibido.

A exibição da Web impressoras mostrada na ilustração anterior é semelhante ao estilo Clássico, porque o modelo de exibição da Web subjacente (um arquivo .htt) foi escrito dessa forma. A lista de arquivos, por exemplo, não é gerada diretamente pelo modelo de exibição da Web. Ele é criado e exibido por um objeto [**WebViewFolderContents**](webviewfoldercontents.md) hospedado pelo modelo de exibição da Web. Os métodos e as propriedades do objeto permitem que a exibição da Web controle seu layout e obtenha informações sobre itens específicos. O conteúdo e o layout da faixa e do bloco de informações são especificados no modelo de exibição da Web.

Como uma exibição da Web dá suporte a DHTML, o modelo também pode ser usado para lidar com a interação do usuário. Por exemplo, quando um usuário clica em um dos ícones de impressora, o objeto **WebViewFolderIcon** dispara um [**evento SelectionChanged.**](/windows/desktop/shell/application-support-bumper) O modelo usa um manipulador de eventos DHTML escrito em script para recuperar as informações solicitadas e exibi-las no bloco de informações.

Este exemplo simples para a pasta Impressoras não é, de forma alguma, a única maneira de usar uma exibição da Web. Escrevendo seu próprio modelo e, se necessário, objetos, você pode usar uma exibição da Web para exibir informações e interagir com o usuário da maneira que achar mais eficaz. Observe que, no momento, os modelos de exibição da Web exibem apenas pastas virtuais definidas pelo sistema. Embora os desenvolvedores possam criar uma pasta virtual implementando uma extensão de namespace, eles devem usar as técnicas descritas em Extensões de [Namespace](/windows/desktop/shell/nse-works) para exibi-la.

## <a name="using-the-web-view-template"></a>Usando o modelo de exibição da Web

A maneira como os dados são exibidos em uma exibição da Web pode ser personalizada de maneira limitada modificando o arquivo de Desktop.ini de uma pasta. Consulte [Personalização de pastas com Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) para obter detalhes. Uma maneira muito mais flexível e poderosa de personalizar um modo de exibição da Web é criar um modelo de exibição da Web personalizado.

O modelo de exibição da Web controla o que é exibido em uma exibição da Web e como. Ele usa técnicas padrão de HTML, DHTML e script para obter e exibir informações e interagir com o usuário. Esta seção discute como criar uma exibição da Web examinando um modelo simples– Generic.htt.


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



Uma maneira simples de criar seu próprio modelo de exibição da Web é pegar Generic.htt e modificá-lo. Como ele é bastante limitado, você também deve ver outros exemplos mais complexos para obter ideias adicionais. Você pode encontrá-los pesquisando no sistema a extensão .htt usada por todos os modelos de exibição da Web. Se você quiser criar um modelo personalizado para uma pasta, deverá começar com o modelo Folder.htt padrão, que geralmente é armazenado em C: Winnt Web ou \\ \\ C: \\ Windows \\ Web. Observe que esses arquivos são definidos como ocultos, portanto, talvez seja necessário modificar as configurações Windows Explorer para exibi-los. Depois que um arquivo .htt é criado, ele deve ser marcado como somente leitura e oculto.

Os modelos de exibição da Web usam a extensão .htt porque diferem ligeiramente dos documentos .htm convencionais. A principal diferença são várias variáveis especiais em arquivos .htt que o sistema substitui com os valores de namespace atuais. As variáveis %THISDIR% e %THISDIRPATH% representam o nome e o caminho da pasta selecionada no momento. A variável %TEMPLATEDIR% representa a pasta em que as folhas de estilos de exibição da Web são armazenadas.

Como a maioria dos modelos HTML, os arquivos .htt têm duas partes básicas: um corpo e uma cabeça. O corpo do modelo controla o layout básico da exibição da Web e carrega os objetos usados para se comunicar com o namespace e exibir informações. O head contém scripts e funções que fazem tarefas como lidar com o reizing e obter informações da pasta. A maioria dos modelos, incluindo Generic.htt, também inclui uma folha de estilos. Em geral, é melhor incluir as informações da folha de estilos em seu modelo. Folhas de estilos separadas podem não funcionar corretamente quando uma exibição da Web é usada com namespaces remotos.

### <a name="the-template-body"></a>O corpo do modelo

O corpo do modelo especifica o que será apresentado por uma exibição da Web. Também é onde os objetos usados para exibir informações e se comunicar com pastas de namespace são carregados. O layout definido por Generic.htt é semelhante ao mostrado na ilustração da seção anterior. Há três regiões de exibição: a faixa e o bloco de informações no lado esquerdo da exibição e a lista de arquivos à direita.

Todas as regiões são identificadores atribuídos a serem usados pela folha de estilos e DHTML. Conforme discutido na próxima seção, há duas faixas possíveis, com identificadores de "Banner" e "MiniBanner". O identificador da região do bloco de informações é "Informações". O identificador do objeto de lista de arquivos é "FileList". Os detalhes do [layout](#controlling-the-web-view-layout) da região são tratados pela folha de estilos e por uma função do Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), que é discutida posteriormente no capítulo.

### <a name="the-banner-region"></a>A região da faixa

A faixa está localizada na parte superior da exibição, no canto superior esquerdo da exibição da Web. A faixa normal exibe o nome e o ícone da pasta cujo conteúdo é exibido na lista de arquivos à direita. No entanto, se a janela ficar muito curta, talvez não haja espaço abaixo do ícone para exibir informações. Por esse motivo, Generic.htt também define um minibanner que exibe apenas o nome da pasta. As duas faixas são inicialmente definidas como ocultas. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) escolhe qual deles deve ser exibido e o define como "Visible".

A faixa normal para Generic. htt é definida por:


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



A primeira parte da seção de faixa exibe o título com uma regra horizontal abaixo dela. Marcas de tabela são usadas para controlar sua posição. O atributo nowrap está definido para o <TD> marca para evitar quebra automática de texto. O sistema substituirá% THISDIRNAME% pelo nome da pasta atual. Um objeto **WebViewFolderIcon** , com um identificador de "Icon" para simplificar, é então carregado para extrair e exibir o ícone da pasta.

A seção minibanner é semelhante à faixa normal. O formato do título é colocado ligeiramente mais alto e não tem uma regra. Como não há nenhum ícone, o objeto **WebViewFolderIcon** não é carregado.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>A região de informações

A parte da exibição da Web abaixo da faixa é usada para apresentar informações detalhadas sobre o item selecionado. Se nenhum item for selecionado, uma mensagem padrão será mostrada. Como Generic. htt exibe apenas um único bloco de texto, esta seção é bem simples.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



A maior parte do trabalho de coletar as informações é tratada por um [script de informações de pasta](#retrieving-and-displaying-folder-information) que é discutido posteriormente neste capítulo. Ele exibe as informações atribuindo o texto a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

Você pode personalizar facilmente a exibição das informações modificando esses elementos ou incluindo outros. Qualquer coisa que você possa colocar em uma página da Web pode ser usada. Por exemplo, para exibir um link para seu site, você pode adicionar um elemento de âncora após o bloco de texto em Generic. htt.


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



### <a name="the-filelist-region"></a>A região de FileList

Finalmente, Generic. htt carrega um objeto [**WebViewFolderContents**](webviewfoldercontents.md) para a região FileList. Como seu identificador está definido como "FileList", ele será referido como o objeto FileList de agora em diante.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



O objeto FileList é encontrado na maioria dos modos de exibição da Web e atende a várias finalidades. FileList exibe a lista de itens contidos na pasta selecionada com as mesmas opções e aparência que a lista de arquivos no estilo clássico. Quando um item é selecionado, o FileList notifica a exibição da Web acionando um evento [SelectionChanged](#retrieving-and-displaying-folder-information) . O FileList também expõe métodos e propriedades que podem ser usados para recuperar informações sobre itens individuais e controlar a posição e o tamanho de sua área de exibição.

Embora o objeto FileList seja muito útil, ele retorna apenas informações padrão do sistema de arquivos, como o tamanho do arquivo ou os atributos. Para recuperar outros tipos de informações de uma pasta do Shell, você precisará carregar e manipular objetos adicionais. Qualquer objeto que possa ser hospedado por uma página da Web pode ser usado com um modo de exibição da Web.

### <a name="the-template-head"></a>O cabeçalho do modelo

O cabeçalho do modelo de exibição da Web contém os scripts e funções que fazem a maior parte do trabalho real. Há duas tarefas essenciais que precisam ser tratadas. Um é o layout do modo de exibição da Web, que precisa ser ajustado para acomodar diferentes regiões de exibição. A outra é recuperar e exibir informações da pasta quando um item é selecionado. Assim como nas folhas de estilo, é melhor incluir todos os scripts e funções no modelo em vez de fazer referência a eles como arquivos separados.

### <a name="controlling-the-web-view-layout"></a>Controlando o layout da exibição da Web

a área disponível para uma exibição da web depende do tamanho da janela de exibição da web e de quanto ela é executada pela barra do Windows Explorer. essa área será alterada sempre que a janela ou a barra do Windows Explorer for redimensionada. Portanto, o layout precisa ser correspondido à área disponível quando uma exibição da Web é carregada e alterada adequadamente quando é redimensionada. Grande parte do layout é especificada na folha de estilos. A região de informações, por exemplo, é definida para ocupar os 30% mais à esquerda da exibição da Web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Como uma exibição da Web é redimensionada, a largura da região de informações será alterada para manter esse percentual. O [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gerencia os problemas de layout que não podem ser manipulados por uma folha de estilos.

### <a name="loading-and-initializing-the-web-view"></a>Carregando e inicializando a exibição da Web

Quando uma exibição da Web é carregada, o layout precisa ser ajustado para se ajustar à área de exibição disponível. Como nenhum item foi selecionado ainda, exibições da Web normalmente exibem algumas informações padrão que se aplicam à pasta inteira. Para lidar com a inicialização, o <BODY> a marca para Generic. htt detecta o evento [OnLoad](/previous-versions//ms531409(v=vs.85)) e chama a função **init** .


```
<body scroll=no onload="Init">
                    
```



**Init** é uma função simples de JScript.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** associa [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ao evento [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) para que ele seja chamado sempre que a área de exibição da Web exibir for alterada. Em seguida, ele executa FixSize para definir o layout inicial e atribui o \_ texto introdutório de L \_ à região de informações. L \_ \_ texto introdutório é um bloco de texto introdutório que é definido na seção folha de estilos.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Ajustando o layout usando a função FixSize

A função [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) é usada para especificar vários aspectos do layout que não podem ser manipulados pela folha de estilos.

Há duas faixas possíveis que podem ser usadas, dependendo da altura da exibição da Web.


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



Generic. htt usa uma altura de 200 pixels como a linha de divisão entre normal e minibanners. Ele define o estilo da faixa selecionada como visível e a outra como oculta. Ele também define várias propriedades de layout para as regiões info e FileList para que caibam corretamente com a faixa selecionada.

Se uma exibição da Web se tornar muito estreita, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usará a largura total da área de exibição para a exibição de FileList.


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



Generic. htt usa 400 pixels como a linha de divisão entre monitores estreitos e largos. Se a exibição da Web for muito estreita, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ocultará a região de informações e modificará a propriedade [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) do FileList para que ela preencha toda a região abaixo da faixa.

As poucas linhas finais de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustam várias propriedades de layout com base nos resultados do código anterior. A largura da região de FileList é ajustada para que ela preencha exatamente a parte da exibição da Web não ocupada pela região de informações. A altura da região de informações é dimensionada para caber entre a faixa e a parte inferior da exibição da Web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Recuperando e exibindo informações da pasta

Quando um usuário seleciona um item, o objeto FileList dispara um evento [SelectionChanged](#retrieving-and-displaying-folder-information) . Esse evento é tratado por um script JScript. Para simplificar, o script encontrado em Generic. htt pressupõe que apenas um item pode ser selecionado de cada vez.


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



O script usa duas propriedades de FileList, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)e [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) para obter informações sobre o item. **FileList. FocusedItem** identifica o item selecionado, com o nome do item fornecido por **FileList.FocusedItem.Name**. **FileList. Folder** é, na verdade, um ponteiro para um objeto de [**pasta**](../shell/folder.md) . O método [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) do objeto de pasta é usado para recuperar as informações restantes sobre o item.

Todas as informações são concatenadas em uma única cadeia de texto, separadas por <BR> marcas para facilitar a leitura. Em seguida, o texto é exibido atribuindo-o a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

## <a name="summary"></a>Resumo

este capítulo descreve algumas das técnicas que você pode usar para personalizar a maneira como o Windows Explorer exibe informações sobre pastas do Shell. A criação de um arquivo de Desktop.ini permite que você faça uma personalização simples, como exibir um ícone personalizado no lugar do ícone de pasta padrão. Quando uma pasta é exibida em uma exibição da Web, seu layout e exibição são controlados por um modelo baseado em HTML que determina quais informações são exibidas e como. Você pode exercer um alto grau de controle sobre a exibição da Web de uma pasta usando HTML, DHTML e técnicas de script padrão para criar um modelo personalizado.

 

 