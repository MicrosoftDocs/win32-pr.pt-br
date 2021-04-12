---
description: O agente de autenticação da Web é criado na parte superior das mesmas tecnologias que alimentam o Internet Explorer no Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considerações para o desenvolvimento de páginas da Web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296850"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="f2135-103">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="f2135-103">Considerations for the web page development</span></span>

<span data-ttu-id="f2135-104">O agente de autenticação da Web é criado na parte superior das mesmas tecnologias que alimentam o Internet Explorer no Windows.</span><span class="sxs-lookup"><span data-stu-id="f2135-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="f2135-105">No entanto, devido a uma finalidade muito especial desse componente, alguns recursos do Internet Explorer foram desabilitados ou bloqueados para configuração específica.</span><span class="sxs-lookup"><span data-stu-id="f2135-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="f2135-106">Além disso, o agente de autenticação da Web fornece um canal de log de eventos dedicado para ajudar a solucionar problemas com páginas que ele processa.</span><span class="sxs-lookup"><span data-stu-id="f2135-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="f2135-107">Modo de documento padrão do Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="f2135-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="f2135-108">O agente de autenticação da Web exibe todas as páginas no "modo de padrões IE10".</span><span class="sxs-lookup"><span data-stu-id="f2135-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="f2135-109">Você pode usar as ferramentas de desenvolvedor no Internet Explorer para ver como sua página funciona em diferentes modos de documento.</span><span class="sxs-lookup"><span data-stu-id="f2135-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="f2135-110">Para obter mais informações sobre a compatibilidade com o Internet Explorer 10, consulte os tópicos do MSDN para o [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2135-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="f2135-111">Recursos desabilitados e bloqueados</span><span class="sxs-lookup"><span data-stu-id="f2135-111">Disabled and locked down features</span></span>

<span data-ttu-id="f2135-112">Vários recursos do Internet Explorer são completamente desabilitados ou bloqueados para valores específicos que não podem ser alterados nas opções da Internet do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f2135-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="f2135-113">Recurso</span><span class="sxs-lookup"><span data-stu-id="f2135-113">Feature</span></span>                            | <span data-ttu-id="f2135-114">Status</span><span class="sxs-lookup"><span data-stu-id="f2135-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2135-115">API de cache de aplicativo ("AppCache")</span><span class="sxs-lookup"><span data-stu-id="f2135-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="f2135-116">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f2135-117">Histórico de link</span><span class="sxs-lookup"><span data-stu-id="f2135-117">Link history</span></span>                       | <span data-ttu-id="f2135-118">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f2135-119">Arquivos temporários</span><span class="sxs-lookup"><span data-stu-id="f2135-119">Temporary files</span></span>                    | <span data-ttu-id="f2135-120">habilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="f2135-121">Cookies</span><span class="sxs-lookup"><span data-stu-id="f2135-121">Cookies</span></span>                            | <span data-ttu-id="f2135-122">Os cookies de sessão estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="f2135-122">Session cookies are enabled.</span></span> <span data-ttu-id="f2135-123">Cookies persistentes são permitidos, mas estão sujeitos a limpeza automática, a menos que o agente de autenticação da Web esteja no modo SSO.</span><span class="sxs-lookup"><span data-stu-id="f2135-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="f2135-124">Para obter mais informações, consulte a seção logon único.</span><span class="sxs-lookup"><span data-stu-id="f2135-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="f2135-125">BD de índice</span><span class="sxs-lookup"><span data-stu-id="f2135-125">Index DB</span></span>                           | <span data-ttu-id="f2135-126">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f2135-127">Armazenamento DOM</span><span class="sxs-lookup"><span data-stu-id="f2135-127">DOM storage</span></span>                        | <span data-ttu-id="f2135-128">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f2135-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="f2135-129">ActiveX</span></span>                            | <span data-ttu-id="f2135-130">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f2135-131">Downloads de arquivos</span><span class="sxs-lookup"><span data-stu-id="f2135-131">File downloads</span></span>                     | <span data-ttu-id="f2135-132">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f2135-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="f2135-133">Requisito de HTTPS</span><span class="sxs-lookup"><span data-stu-id="f2135-133">HTTPS requirement</span></span>

<span data-ttu-id="f2135-134">A primeira URL que um aplicativo usará para se comunicar com o provedor online precisa ser HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f2135-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="f2135-135">Dimensão para diferentes tamanhos de janela</span><span class="sxs-lookup"><span data-stu-id="f2135-135">Dimension for different window sizes</span></span>

<span data-ttu-id="f2135-136">Um aplicativo do Windows 8 pode aparecer em vários tamanhos diferentes, como tela inteira, uma janela redimensionada ou dentro de um botão, como um botão de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f2135-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="f2135-137">Dependendo de qual layout da janela o agente de autenticação da Web aparece, o tamanho com o qual as páginas da Web precisam funcionar pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="f2135-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="f2135-138">Para obter mais informações, consulte o tópico [diretrizes para redimensionamento para layouts estreitos](/previous-versions/windows/hh465371(v=win.10)) e o tópico [diretrizes para compartilhamento de conteúdo](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="f2135-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="f2135-139">A página da Web deve usar consultas de mídia do CSS para verificar o tamanho com o qual deve trabalhar e se ajustar de acordo.</span><span class="sxs-lookup"><span data-stu-id="f2135-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="f2135-140">No entanto, a página não deve ser projetada com base nos pixels exatos documentados aqui e deve ser capaz de dimensionar para tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f2135-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="f2135-141">Os tamanhos especificados neste documento estão sujeitos a alterações em versões futuras do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f2135-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="f2135-142">Se uma página não puder se ajustar a todas as informações no espaço alocado (por exemplo, uma longa lista de permissões que um aplicativo está solicitando), o agente de autenticação da Web fornecerá barras de rolagem para permitir que o usuário Role a página conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f2135-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="f2135-143">O zoom também é fornecido pelo pinçar zoom para dispositivos baseados em toque e CTRL + roda do mouse para PCs desktop e laptop.</span><span class="sxs-lookup"><span data-stu-id="f2135-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="f2135-144">Para testar diferentes fatores de dimensionamento, use o [aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) carregado no Microsoft Visual Studio Professional 2012, que permite simular a tela inteira e os Estados redimensionados.</span><span class="sxs-lookup"><span data-stu-id="f2135-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="f2135-145">Além de layouts diferentes documentados acima, certifique-se de testar sua página em uma orientação de tela diferente (por exemplo, retrato e paisagem) e localidades e idiomas diferentes, bem como com recursos de acessibilidade, como a opção "tornar tudo maior" ativada.</span><span class="sxs-lookup"><span data-stu-id="f2135-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="f2135-146">Os layouts disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="f2135-146">The available layouts are:</span></span>

-   [<span data-ttu-id="f2135-147">Tela inteira</span><span class="sxs-lookup"><span data-stu-id="f2135-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="f2135-148">Janela redimensionada</span><span class="sxs-lookup"><span data-stu-id="f2135-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="f2135-149">Exibição de botão</span><span class="sxs-lookup"><span data-stu-id="f2135-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="f2135-150">Exibição do seletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="f2135-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="f2135-151">Tela inteira</span><span class="sxs-lookup"><span data-stu-id="f2135-151">Full screen</span></span>

<span data-ttu-id="f2135-152">Para o layout de tela inteira, as dimensões da página da Web são:</span><span class="sxs-lookup"><span data-stu-id="f2135-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="f2135-153">Largura: 566 pixels</span><span class="sxs-lookup"><span data-stu-id="f2135-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="f2135-154">Altura: altura da tela (depende da resolução da tela)</span><span class="sxs-lookup"><span data-stu-id="f2135-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="f2135-155">O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web no layout de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="f2135-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![um exemplo de interface do usuário do agente de autenticação da Web no layout de tela inteira](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="f2135-157">Redimensionado</span><span class="sxs-lookup"><span data-stu-id="f2135-157">Resized</span></span>

<span data-ttu-id="f2135-158">Para uma janela redimensionada, as dimensões da página da Web podem ser:</span><span class="sxs-lookup"><span data-stu-id="f2135-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="f2135-159">Largura: 260 pixels</span><span class="sxs-lookup"><span data-stu-id="f2135-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="f2135-160">Altura: altura da tela (depende da resolução da tela)</span><span class="sxs-lookup"><span data-stu-id="f2135-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="f2135-161">O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web em uma janela redimensionada na página da Web do XBox.</span><span class="sxs-lookup"><span data-stu-id="f2135-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="f2135-162">Observe que a interface do usuário do agente de autenticação da Web está apenas no lado direito da captura de tela.</span><span class="sxs-lookup"><span data-stu-id="f2135-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![um exemplo de interface do usuário do agente de autenticação da Web em uma janela redimensionada](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="f2135-164">Exibição de botão</span><span class="sxs-lookup"><span data-stu-id="f2135-164">Charm view</span></span>

<span data-ttu-id="f2135-165">Para a exibição de botão, as dimensões da página da Web são:</span><span class="sxs-lookup"><span data-stu-id="f2135-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="f2135-166">Largura: 566 pixels</span><span class="sxs-lookup"><span data-stu-id="f2135-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="f2135-167">Altura: altura da tela (depende da resolução da tela)</span><span class="sxs-lookup"><span data-stu-id="f2135-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="f2135-168">O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web na exibição de botão.</span><span class="sxs-lookup"><span data-stu-id="f2135-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![um exemplo mostra a interface do usuário do agente de autenticação da Web na exibição de botão](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="f2135-170">Exibição do seletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="f2135-170">File picker view</span></span>

<span data-ttu-id="f2135-171">Para a exibição do seletor de arquivo, as dimensões da página da Web são:</span><span class="sxs-lookup"><span data-stu-id="f2135-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="f2135-172">Largura: 566 pixels</span><span class="sxs-lookup"><span data-stu-id="f2135-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="f2135-173">Altura: altura da tela (depende da resolução da tela)</span><span class="sxs-lookup"><span data-stu-id="f2135-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="f2135-174">O exemplo a seguir mostra a interface do usuário do agente de autenticação da Web na exibição do seletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f2135-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![um exemplo mostra a interface do usuário do agente de autenticação da Web na exibição do seletor de arquivos](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="f2135-176">Nenhuma nova janela por padrão</span><span class="sxs-lookup"><span data-stu-id="f2135-176">No new windows by default</span></span>

<span data-ttu-id="f2135-177">Por padrão, nenhuma URL fará com que uma nova janela seja aberta, mas será exibida na janela do agente de autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="f2135-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="f2135-178">Isso inclui o método de JavaScript Window. Open, o atributo "target" dos hiperlinks ou quando o usuário usa o mecanismo Ctrl + clique para forçar a abertura de uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="f2135-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="f2135-179">A exceção a essa regra é quando uma página da Web declara um link como seguro para ser navegado em um navegador, conforme descrito no destino de personalização dos hiperlinks.</span><span class="sxs-lookup"><span data-stu-id="f2135-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2135-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2135-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2135-181">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="f2135-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="f2135-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="f2135-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
