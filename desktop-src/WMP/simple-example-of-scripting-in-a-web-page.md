---
title: Exemplo simples de script em uma página da Web
description: Exemplo simples de script em uma página da Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Controle ActiveX do Windows Media Player, exemplo de script
- Controle ActiveX móvel do Windows Media Player, exemplo de script
- Controle ActiveX, exemplo de script
- inserindo, páginas da Web
- Inserção de página da Web, exemplo de script
- exemplo de script para inserção de página da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105763290"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="04dd4-119">Exemplo simples de script em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="04dd4-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="04dd4-120">Você pode facilmente inserir o controle do Windows Media Player em um arquivo HTML usando qualquer linguagem de script que seu navegador reconhece.</span><span class="sxs-lookup"><span data-stu-id="04dd4-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="04dd4-121">O exemplo simples a seguir usa o Microsoft JScript para criar uma página que irá reproduzir um arquivo quando você clicar em um botão e parar de executar o arquivo quando você clicar em outro botão.</span><span class="sxs-lookup"><span data-stu-id="04dd4-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="04dd4-122">Você pode inserir o controle ActiveX do Windows Media Player em uma página da Web usando as quatro etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="04dd4-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="04dd4-123">Crie a página da Web.</span><span class="sxs-lookup"><span data-stu-id="04dd4-123">Create the webpage.</span></span>
2.  <span data-ttu-id="04dd4-124">Adicione a marca do objeto.</span><span class="sxs-lookup"><span data-stu-id="04dd4-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="04dd4-125">Adicione uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="04dd4-125">Add a user interface.</span></span> <span data-ttu-id="04dd4-126">Nesse caso, dois botões.</span><span class="sxs-lookup"><span data-stu-id="04dd4-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="04dd4-127">Adicione algumas linhas de código para responder quando o usuário clicar em um dos botões que você criou.</span><span class="sxs-lookup"><span data-stu-id="04dd4-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="04dd4-128">Criando a página da Web</span><span class="sxs-lookup"><span data-stu-id="04dd4-128">Creating the Web Page</span></span>

<span data-ttu-id="04dd4-129">A primeira etapa é criar uma página da Web HTML válida.</span><span class="sxs-lookup"><span data-stu-id="04dd4-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="04dd4-130">O código a seguir é o mínimo necessário para criar uma página HTML em branco, mas válida:</span><span class="sxs-lookup"><span data-stu-id="04dd4-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="04dd4-131">Adicionando a marca do objeto</span><span class="sxs-lookup"><span data-stu-id="04dd4-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="04dd4-132">Depois de criar uma página da Web, você precisa adicionar uma marca de objeto.</span><span class="sxs-lookup"><span data-stu-id="04dd4-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="04dd4-133">Isso identifica o controle ActiveX para o navegador e configura todas as definições iniciais.</span><span class="sxs-lookup"><span data-stu-id="04dd4-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="04dd4-134">Você deve posicionar a marca de objeto no corpo do código.</span><span class="sxs-lookup"><span data-stu-id="04dd4-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="04dd4-135">Se você colocá-lo no corpo, a interface do usuário padrão do Windows Media Player será visível.</span><span class="sxs-lookup"><span data-stu-id="04dd4-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="04dd4-136">Se você quiser criar sua própria interface de usuário, defina os atributos de altura e largura como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="04dd4-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="04dd4-137">Você também pode definir o *Player*. Propriedade **UIMODE** como "invisível" quando você deseja ocultar o controle, mas ainda reservar espaço para ele na página.</span><span class="sxs-lookup"><span data-stu-id="04dd4-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="04dd4-138">O código a seguir é recomendado quando você fornece uma interface do usuário personalizada:</span><span class="sxs-lookup"><span data-stu-id="04dd4-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="04dd4-139">Os seguintes atributos de marca de objeto são necessários:</span><span class="sxs-lookup"><span data-stu-id="04dd4-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="04dd4-140">ID</span><span class="sxs-lookup"><span data-stu-id="04dd4-140">ID</span></span>

<span data-ttu-id="04dd4-141">O nome que será usado por outras partes do código para identificar e usar o controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="04dd4-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="04dd4-142">Você pode escolher qualquer nome desejado, desde que ele seja um nome que ainda não esteja sendo usado por HTML, por extensões HTML ou pela linguagem de script que você está usando.</span><span class="sxs-lookup"><span data-stu-id="04dd4-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="04dd4-143">Neste exemplo, o nome "Player" é usado, mas você também pode chamá-lo de "myplayr" ou algo mais.</span><span class="sxs-lookup"><span data-stu-id="04dd4-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="04dd4-144">Basta escolher um nome que seja exclusivo para essa página da Web.</span><span class="sxs-lookup"><span data-stu-id="04dd4-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="04dd4-145">CLASSID</span><span class="sxs-lookup"><span data-stu-id="04dd4-145">CLASSID</span></span>

<span data-ttu-id="04dd4-146">Um número hexadecimal muito grande que é exclusivo para o controle.</span><span class="sxs-lookup"><span data-stu-id="04dd4-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="04dd4-147">Apenas um controle tem esse número e é o controle ActiveX do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="04dd4-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="04dd4-148">Para evitar erros tipográficos, você pode copiar e colar esse número da documentação.</span><span class="sxs-lookup"><span data-stu-id="04dd4-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="04dd4-149">As versões do controle do Windows Media Player anteriores à versão 7,0 tinham um ClassID diferente.</span><span class="sxs-lookup"><span data-stu-id="04dd4-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="04dd4-150">Adicionando uma interface do usuário</span><span class="sxs-lookup"><span data-stu-id="04dd4-150">Adding a User Interface</span></span>

<span data-ttu-id="04dd4-151">O HTML permite uma vasta gama de elementos da interface do usuário, permitindo que o usuário interaja com sua página da Web clicando, pressionando chaves e outras ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="04dd4-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="04dd4-152">Adicionar alguns botões de entrada é a maneira mais fácil de fornecer uma interface de usuário rápida.</span><span class="sxs-lookup"><span data-stu-id="04dd4-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="04dd4-153">O código a seguir cria dois botões que podem responder ao usuário.</span><span class="sxs-lookup"><span data-stu-id="04dd4-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="04dd4-154">Clicar em um botão inicia o fluxo de mídia em execução e o outro botão o interrompe:</span><span class="sxs-lookup"><span data-stu-id="04dd4-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="04dd4-155">O nome do botão é usado para identificar o botão para seu código; o valor é o rótulo que será exibido no botão e o atributo OnClick identificará qual parte do seu código de script será chamada quando o botão for clicado.</span><span class="sxs-lookup"><span data-stu-id="04dd4-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="04dd4-156">Adicionando código de script</span><span class="sxs-lookup"><span data-stu-id="04dd4-156">Adding Scripting Code</span></span>

<span data-ttu-id="04dd4-157">O código de script adiciona interatividade à sua página.</span><span class="sxs-lookup"><span data-stu-id="04dd4-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="04dd4-158">O código de script pode responder a eventos, chamar métodos e alterar as propriedades de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="04dd4-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="04dd4-159">Os scripts estendidos são colocados em um conjunto de marcas de SCRIPT.</span><span class="sxs-lookup"><span data-stu-id="04dd4-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="04dd4-160">A marca de SCRIPT informa ao navegador onde está o código de script e identifica a linguagem de script.</span><span class="sxs-lookup"><span data-stu-id="04dd4-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="04dd4-161">Se você não identificar um idioma, o idioma padrão será Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="04dd4-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="04dd4-162">É uma boa prática de criação colocar o script em marcas de comentário HTML para que os navegadores que não dão suporte a scripts não processem seu código como texto.</span><span class="sxs-lookup"><span data-stu-id="04dd4-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="04dd4-163">Coloque a marca de SCRIPT em qualquer lugar dentro do corpo do arquivo HTML e insira o código de comentário entre as marcas de SCRIPT de abertura e fechamento.</span><span class="sxs-lookup"><span data-stu-id="04dd4-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="04dd4-164">O exemplo de código do Microsoft JScript a seguir chama o controle do Windows Media Player e executa uma ação apropriada em resposta ao clique no botão correspondente.</span><span class="sxs-lookup"><span data-stu-id="04dd4-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="04dd4-165">A função de exemplo, StartMeUp, é chamada quando o botão marcado como executar é clicado e a função ShutMeDown é chamada quando o botão parar é clicado.</span><span class="sxs-lookup"><span data-stu-id="04dd4-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="04dd4-166">O código dentro de StartMeUp usa a propriedade URL para definir um caminho para a mídia.</span><span class="sxs-lookup"><span data-stu-id="04dd4-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="04dd4-167">A mídia começará a ser reproduzida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="04dd4-167">The media will start playing immediately.</span></span>

<span data-ttu-id="04dd4-168">O código ShutMeDown chama o método **Stop** do objeto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="04dd4-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="04dd4-169">Observe que o objeto **Controls** é chamado por meio da propriedade **Controls** do objeto **Player** , que tem o valor de ID de "Player".</span><span class="sxs-lookup"><span data-stu-id="04dd4-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="04dd4-170">O código a seguir mostra um exemplo completo.</span><span class="sxs-lookup"><span data-stu-id="04dd4-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="04dd4-171">Observe que você deve fornecer uma URL válida para um nome de arquivo válido na propriedade URL.</span><span class="sxs-lookup"><span data-stu-id="04dd4-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="04dd4-172">Nesse caso, a suposição é que o arquivo Laure. WMA esteja no mesmo diretório que o arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="04dd4-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04dd4-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04dd4-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04dd4-174">**Usando o controle do Windows Media Player em uma página da Web**</span><span class="sxs-lookup"><span data-stu-id="04dd4-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




