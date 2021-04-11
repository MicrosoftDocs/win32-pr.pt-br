---
description: Este tópico descreve as práticas recomendadas para a criação de páginas da Web que usam o agente de autenticação da Web para fazer logon.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Melhores práticas para o design de páginas da Web de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296522"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="3745d-103">Melhores práticas para o design de páginas da Web de autenticação</span><span class="sxs-lookup"><span data-stu-id="3745d-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="3745d-104">Este tópico descreve as práticas recomendadas para a criação de páginas da Web que usam o agente de autenticação da Web para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="3745d-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="3745d-105">Uso de metamarcações</span><span class="sxs-lookup"><span data-stu-id="3745d-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="3745d-106">Uso do estilo de CSS do Windows 8</span><span class="sxs-lookup"><span data-stu-id="3745d-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="3745d-107">Uso de cores e temas</span><span class="sxs-lookup"><span data-stu-id="3745d-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="3745d-108">Alinhamento</span><span class="sxs-lookup"><span data-stu-id="3745d-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="3745d-109">Projetando para ajuste</span><span class="sxs-lookup"><span data-stu-id="3745d-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="3745d-110">Projetando para uma experiência de logon rápida e fluida</span><span class="sxs-lookup"><span data-stu-id="3745d-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="3745d-111">Considerações sobre segurança</span><span class="sxs-lookup"><span data-stu-id="3745d-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="3745d-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3745d-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="3745d-113">Uso de metamarcações</span><span class="sxs-lookup"><span data-stu-id="3745d-113">Use of metatags</span></span>

<span data-ttu-id="3745d-114">Usando metamarcações, o provedor "contoso social" pode especificar o título, o ícone e a cor do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="3745d-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="3745d-115">No arquivo HTML de exemplo (WebAuthLogin.html), isso é feito usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="3745d-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="3745d-116">Isso permite que o Windows integre a presença do provedor de uma maneira proeminente no cabeçalho da interface do usuário, conforme realçado pela caixa vermelha na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3745d-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![página de logon mostrando o cabeçalho da Contoso na interface do usuário](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="3745d-118">Uso do estilo de CSS do Windows 8</span><span class="sxs-lookup"><span data-stu-id="3745d-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="3745d-119">A folha de estilos UI-Light. css fornecida é a folha de estilos do Windows 8 usada pelos aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3745d-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="3745d-120">Ele define o estilo do aplicativo da Windows Store para controles de tipografia e padrão, como botões, caixas de texto, hiperlinks e caixas de seleção para garantir que eles sejam amigáveis para toque.</span><span class="sxs-lookup"><span data-stu-id="3745d-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="3745d-121">Ao criar e adaptar páginas de autorização da Web para o Windows 8, incentivamos você a usar essa folha de estilo como está e atualizá-la conforme necessário, desde que sua página da Web ainda siga as práticas recomendadas da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="3745d-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="3745d-122">Por exemplo, se você tiver uma folha de estilos especial para o que os hiperlinks devem parecer na sua página da Web, é bom ter a sorte de ter certeza de que o estilo que você fornece é amigável de toque da mesma forma que os hiperlinks padrão do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3745d-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="3745d-123">Isso é essencial para a base de consumidores usando o Windows 8 em seus dispositivos de toque.</span><span class="sxs-lookup"><span data-stu-id="3745d-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="3745d-124">Uso de cores e temas</span><span class="sxs-lookup"><span data-stu-id="3745d-124">Use of color and themes</span></span>

<span data-ttu-id="3745d-125">Este exemplo demonstra um uso muito elaborado de cores de algumas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="3745d-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="3745d-126">Plano de fundo branco da página da Web.</span><span class="sxs-lookup"><span data-stu-id="3745d-126">White background for the web page.</span></span> <span data-ttu-id="3745d-127">Como você pode ver na captura de tela anterior, a página da Web é hospedada dentro de uma superfície branca que abrange a largura do ecrã.</span><span class="sxs-lookup"><span data-stu-id="3745d-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="3745d-128">Para garantir que a página da Web se integre com a superfície, é recomendável que a página da Web tenha um plano de fundo branco.</span><span class="sxs-lookup"><span data-stu-id="3745d-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="3745d-129">Colorir controles com base na sua cor de marca.</span><span class="sxs-lookup"><span data-stu-id="3745d-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="3745d-130">O arquivo CSS Theme-Colors. css fornece estilos para substituir as cores padrão dos controles na folha de estilo da interface do usuário-Light para coincidir com os controles com a cor do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="3745d-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="3745d-131">Por exemplo, na captura de tela a seguir, os botões e hiperlinks assumem cores derivadas da cor do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="3745d-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![captura de tela dos botões e do texto com a mesma cor que o cabeçalho](images/wab-figure11.png)
-   <span data-ttu-id="3745d-133">Cor do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="3745d-133">Header color.</span></span> <span data-ttu-id="3745d-134">O uso da cor da marca da Contoso no cabeçalho cria uma personalidade unificada para a marca do provedor na interface do usuário do sistema.</span><span class="sxs-lookup"><span data-stu-id="3745d-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="3745d-135">Alinhamento</span><span class="sxs-lookup"><span data-stu-id="3745d-135">Alignment</span></span>

<span data-ttu-id="3745d-136">A página da Web não tem nenhum preenchimento à esquerda ou à direita para permitir o alinhamento tipográfico com o título no cabeçalho à esquerda e o ícone no cabeçalho à direita.</span><span class="sxs-lookup"><span data-stu-id="3745d-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="3745d-137">Você também observará que os botões estão sempre alinhados na parte inferior direita na página da Web (e alinhados à direita com o ícone no cabeçalho).</span><span class="sxs-lookup"><span data-stu-id="3745d-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="3745d-138">Essa é a melhor prática, pois os usuários do Windows 8 estarão acostumados com fluxos de caixa de diálogo semelhantes com botões no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="3745d-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="3745d-139">Projetando para ajuste</span><span class="sxs-lookup"><span data-stu-id="3745d-139">Designing for snap</span></span>

<span data-ttu-id="3745d-140">Na imagem a seguir, você pode ver as páginas de logon e permissões no estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3745d-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="3745d-141">exibição de ajuste da tela de logon</span><span class="sxs-lookup"><span data-stu-id="3745d-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="3745d-142">.</span><span class="sxs-lookup"><span data-stu-id="3745d-142">.</span></span> ![<span data-ttu-id="3745d-143">exibição de ajuste da página de permissões</span><span class="sxs-lookup"><span data-stu-id="3745d-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="3745d-144">No arquivo de exemplo UI-webauth. CSS, você pode ver o uso de consultas de mídia que otimizam o layout da página para ajuste de estado com base na largura disponível para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="3745d-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="3745d-145">O trecho de código incluído no escopo a seguir implementa o CSS adaptado para o estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3745d-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="3745d-146">No Windows 8, a largura do estado de ajuste é de 320 pixels.</span><span class="sxs-lookup"><span data-stu-id="3745d-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="3745d-147">A página de autenticação da Web ocupa 260 pixels na interface do usuário acima.</span><span class="sxs-lookup"><span data-stu-id="3745d-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="3745d-148">Estamos usando um valor de largura máxima com margem suficiente, portanto, o código de consulta de mídia do provedor não está associado à largura exata do estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3745d-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="3745d-149">Ao personalizar seu aplicativo para o modo de exibição de ajuste, é importante que o usuário não perca nenhum contexto que tenha nas outras exibições da experiência de autenticação da Web (exibições completa, de preenchimento ou de botão), mas é importante reestruturar o layout e a hierarquia dos elementos na página para que as informações necessárias para manter o contexto sejam visíveis e interativas.</span><span class="sxs-lookup"><span data-stu-id="3745d-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="3745d-150">Nós chamamos alguns exemplos de como a amostra destaca a página da Web para o estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3745d-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="3745d-151">Por exemplo, para a página de logon no estado de ajuste, a propriedade Width do campo de texto de entrada (conforme especificado em UI-Light. css) foi substituída e definida como um valor numérico menor, de modo que o campo de texto não seja cortado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="3745d-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="3745d-152">Como outro exemplo, no estado de ajuste, o tamanho da fonte dos cabeçalhos H1 e H2 é reduzido para 20 pt e 11 pt de 42 pt e 20 pt, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3745d-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="3745d-153">Isso é feito de acordo com a rampa de tipo do Windows 8 e otimiza o texto para ser mais compacto no visor alterado.</span><span class="sxs-lookup"><span data-stu-id="3745d-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="3745d-154">Como outro exemplo, observe que os tamanhos dos ícones na página permissões são menores (compare com a página de exibição completa acima).</span><span class="sxs-lookup"><span data-stu-id="3745d-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="3745d-155">Novamente, isso é feito para manter o contexto, ao mesmo tempo que troca ativos de design para aqueles mais ideais para o visor alterado.</span><span class="sxs-lookup"><span data-stu-id="3745d-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="3745d-156">Projetando para uma experiência de logon rápida e fluida</span><span class="sxs-lookup"><span data-stu-id="3745d-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="3745d-157">No início da criação desta página da Web, fizemos um jogo no chão de que uma coisa que essa página é melhor é uma experiência de logon rápida e fluida.</span><span class="sxs-lookup"><span data-stu-id="3745d-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="3745d-158">Assim, a interface do usuário que é mais proeminente no fluxo é o campo nome de usuário e senha na página de logon para uma experiência de entrada de credenciais rápida.</span><span class="sxs-lookup"><span data-stu-id="3745d-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="3745d-159">Enquanto identificamos que há outros cenários comuns, como recuperação de senha, e referência de declarações de privacidade, a rica experiência da Web é um lugar melhor para essas experiências.</span><span class="sxs-lookup"><span data-stu-id="3745d-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="3745d-160">Para todos os fluxos não relacionados à experiência segura da autenticação na Web, é recomendável navegar pelo usuário para o navegador.</span><span class="sxs-lookup"><span data-stu-id="3745d-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="3745d-161">Isso é mostrado no arquivo HTML de exemplo (WebAuthLogin.html) da seguinte maneira: `<meta name="mswebdialog-newwindowurl" content="*" />` isso abre todas as páginas da Web vinculadas da página logon ou permissões no navegador padrão do usuário, em que o usuário pode concluir esses fluxos e, em seguida, retornar ao aplicativo para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="3745d-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="3745d-162">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="3745d-162">Security Considerations</span></span>

<span data-ttu-id="3745d-163">Os artigos a seguir fornecem diretrizes para escrever código C++ seguro.</span><span class="sxs-lookup"><span data-stu-id="3745d-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="3745d-164">Práticas recomendadas de segurança para C++</span><span class="sxs-lookup"><span data-stu-id="3745d-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="3745d-165">[Padrões & práticas de segurança diretrizes para aplicativos](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="3745d-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="3745d-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3745d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3745d-167">Considerações para o desenvolvimento de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="3745d-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="3745d-168">Perguntas frequentes sobre o agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="3745d-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="3745d-169">Aplicativo de exemplo do SDK do agente de autenticação da Web</span><span class="sxs-lookup"><span data-stu-id="3745d-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="3745d-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="3745d-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
