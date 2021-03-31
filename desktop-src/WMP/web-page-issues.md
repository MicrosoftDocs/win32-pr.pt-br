---
title: Problemas de página da Web
description: Problemas de página da Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Listas de reprodução do metarquivo do Windows Media, páginas da Web
- listas de reprodução, páginas da Web
- listas de reprodução de metarquivo, páginas da Web
- Playlists do metarquivo do Windows Media, personalizando HTMLView
- listas de reprodução, personalizando HTMLView
- listas de reprodução de metarquivo, personalizando HTMLView
- Playlists do metarquivo do Windows Media, personalização de HTMLView
- listas de reprodução, personalização de HTMLView
- listas de reprodução de metarquivo, personalização de HTMLView
- Personalizando o HTMLView
- Windows Media Player, páginas da Web
- Windows Media Player, personalizando o HTMLView
- Windows Media Player, HTMLView Personalizando
- HTMLView, personalizando
- HTMLView, páginas da Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636869"
---
# <a name="web-page-issues"></a><span data-ttu-id="92ac1-118">Problemas de página da Web</span><span class="sxs-lookup"><span data-stu-id="92ac1-118">Web Page Issues</span></span>

<span data-ttu-id="92ac1-119">Há algumas coisas a serem consideradas quando você cria uma página da Web a ser exibida no recurso que **agora está executando** o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="92ac1-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="92ac1-120">Esta seção aborda alguns dos problemas que você pode encontrar ao criar seu conteúdo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="92ac1-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="92ac1-121">Personalizando o HTMLView</span><span class="sxs-lookup"><span data-stu-id="92ac1-121">Customizing HTMLView</span></span>

<span data-ttu-id="92ac1-122">Sua página da Web do HTMLView pode ser tão simples ou complexa quanto você desejar.</span><span class="sxs-lookup"><span data-stu-id="92ac1-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="92ac1-123">Você pode incluir qualquer um dos elementos que geralmente usa em seu conteúdo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="92ac1-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="92ac1-124">Se você inserir o controle do Windows Media Player, poderá exibir uma das interfaces de usuário fornecidas pelo controle, criar sua própria interface de usuário usando HTML e código de script, ou não fornecer nenhuma interface de usuários (o que significa que o usuário pode usar os controles de transporte do player de modo completo).</span><span class="sxs-lookup"><span data-stu-id="92ac1-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="92ac1-125">O tamanho recomendado para páginas da Web exibidas usando o recurso HTMLView é 575 x 345 pixels.</span><span class="sxs-lookup"><span data-stu-id="92ac1-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="92ac1-126">O usuário, no entanto, tem a capacidade de redimensionar o Windows Media Player e escolher a resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="92ac1-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="92ac1-127">Se a página da Web HTMLView for maior do que o tamanho acomodado pelo recurso em **execução** , o Player exibirá as barras de rolagem horizontal e vertical que permitem que o usuário veja a página inteira.</span><span class="sxs-lookup"><span data-stu-id="92ac1-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="92ac1-128">Você deve testar o conteúdo do HTMLView usando uma variedade de resoluções de tela e tamanhos de Player para determinar o melhor tamanho para sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="92ac1-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="92ac1-129">O Windows Media Player não fornece um método que permite que você especifique um tamanho para o player de modo completo.</span><span class="sxs-lookup"><span data-stu-id="92ac1-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="92ac1-130">Navegação de página da Web</span><span class="sxs-lookup"><span data-stu-id="92ac1-130">Web page navigation</span></span>

<span data-ttu-id="92ac1-131">O Windows Media Player não fornece uma barra de ferramentas de navegação para páginas da Web exibidas no recurso **agora em execução** .</span><span class="sxs-lookup"><span data-stu-id="92ac1-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="92ac1-132">Isso significa que você tem controle total sobre se os usuários podem navegar para fora da sua página da Web do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="92ac1-133">Se você quiser permitir que os usuários naveguem para outras páginas da Web, você deve incluir elementos em seu código HTML para fornecer essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="92ac1-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="92ac1-134">Recuperando a janela pai</span><span class="sxs-lookup"><span data-stu-id="92ac1-134">Retrieving the parent window</span></span>

<span data-ttu-id="92ac1-135">Se o código de script existente usar **Window. pai** para recuperar o objeto de janela pai, esse código não funcionará na sua página da Web HtmlView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="92ac1-136">Quando você usa HTMLView, não há nenhum objeto de janela pai; Portanto, esse recurso de script não está disponível.</span><span class="sxs-lookup"><span data-stu-id="92ac1-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="92ac1-137">Sobre o navegador incorporado</span><span class="sxs-lookup"><span data-stu-id="92ac1-137">About the embedded browser</span></span>

<span data-ttu-id="92ac1-138">Como o Windows Media Player usa uma instância incorporada do Internet Explorer para exibir o conteúdo do HTMLView, as configurações do usuário e as políticas do Internet Explorer se aplicam a qualquer página da Web exibida no Player.</span><span class="sxs-lookup"><span data-stu-id="92ac1-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="92ac1-139">Por exemplo, se o usuário tiver configurado o Internet Explorer para impedir que as páginas da Web baixem cookies para o computador, sua página da Web do HTMLView também será impedida de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="92ac1-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="92ac1-140">As páginas da Web abertas usando o recurso HTMLView sempre são executadas na zona de segurança da **Internet** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="92ac1-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="92ac1-141">O controle de navegador da Web incorporado usa as mesmas regras para armazenar em cache as páginas a partir da versão autônoma do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="92ac1-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="92ac1-142">É uma boa ideia usar páginas de Active Server (ASP) ao criar seu conteúdo para garantir que o conteúdo seja entregue do seu servidor Web cada vez que o Windows Media Player acessar a página Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="92ac1-143">O uso de páginas ASP pode ser tão simples quanto renomear sua página da Web para usar uma extensão de nome de arquivo. ASP.</span><span class="sxs-lookup"><span data-stu-id="92ac1-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="92ac1-144">Sobre o conteúdo da Web local</span><span class="sxs-lookup"><span data-stu-id="92ac1-144">About local Web content</span></span>

<span data-ttu-id="92ac1-145">O recurso HTMLView não permite que você abra páginas da Web armazenadas no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="92ac1-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="92ac1-146">Solicitando ao usuário</span><span class="sxs-lookup"><span data-stu-id="92ac1-146">Prompting the user</span></span>

<span data-ttu-id="92ac1-147">Você pode usar **Window. prompt** para solicitar informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="92ac1-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="92ac1-148">No entanto, **Window. Alert** e **Window. Confirm** não estão disponíveis ao usar HtmlView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="92ac1-149">Problemas de tempo</span><span class="sxs-lookup"><span data-stu-id="92ac1-149">Timing issues</span></span>

<span data-ttu-id="92ac1-150">Você pode encontrar problemas de tempo ao usar um controle do Windows Media Player inserido em sua página da Web do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="92ac1-151">No HTMLView, um controle player incorporado compartilha seu mecanismo de reprodução com o Windows Media Player autônomo.</span><span class="sxs-lookup"><span data-stu-id="92ac1-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="92ac1-152">É possível que o Player autônomo possa abrir e começar a reproduzir a primeira entrada da playlist antes da página da Web (e, portanto, o controle do jogador) concluir o carregamento.</span><span class="sxs-lookup"><span data-stu-id="92ac1-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="92ac1-153">Isso significa que, se você manipular os eventos **OpenStateChange** ou **PlayStateChange** , o código do script não receberá notificações de eventos para esses eventos até que o controle do jogador e seus objetos associados sejam carregados.</span><span class="sxs-lookup"><span data-stu-id="92ac1-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="92ac1-154">Você pode executar etapas em seu código para atrasar a reprodução até que o controle do Windows Media Player seja instanciado.</span><span class="sxs-lookup"><span data-stu-id="92ac1-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="92ac1-155">Uma maneira de fazer isso é fazer com que a primeira entrada em sua lista de reprodução de metarquivo aponte para um arquivo de imagem e defina a duração do arquivo com um período de tempo que permita a carga do controle do jogador.</span><span class="sxs-lookup"><span data-stu-id="92ac1-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="92ac1-156">O código de exemplo a seguir demonstra essa opção:</span><span class="sxs-lookup"><span data-stu-id="92ac1-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="92ac1-157">Quando a lista de reprodução anterior é aberta, o Windows Media Player aguarda a primeira entrada da lista de reprodução por até um minuto, enquanto o Player carrega a página da Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="92ac1-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="92ac1-158">Em seguida, em sua página da Web do HTMLView, escreva o código de script para manipular o evento **OnLoad** para o elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="92ac1-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="92ac1-159">Na função do manipulador de eventos, chame o método do Player **. Next** para iniciar a reprodução da segunda entrada na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="92ac1-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="92ac1-160">Quando a página da Web no exemplo anterior termina de carregar, o Windows Media Player avança imediatamente para a segunda entrada na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="92ac1-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="92ac1-161">Isso substitui a duração especificada para o primeiro elemento na lista de reprodução, o que significa que o usuário não precisa aguardar um minuto completo antes de ver o conteúdo desejado; Ele só precisa aguardar a conclusão do carregamento da página da Web.</span><span class="sxs-lookup"><span data-stu-id="92ac1-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="92ac1-162">Como o controle do jogador é completamente instanciado neste ponto, os eventos **OpenStateChange** e **PlayStateChange** podem ser tratados da maneira usual.</span><span class="sxs-lookup"><span data-stu-id="92ac1-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92ac1-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92ac1-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ac1-164">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="92ac1-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="92ac1-165">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="92ac1-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="92ac1-166">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="92ac1-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




