---
title: Fontes de cores
description: Este tópico descreve as fontes de cor, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104552983"
---
# <a name="color-fonts"></a><span data-ttu-id="3c9a4-103">Fontes de cores</span><span class="sxs-lookup"><span data-stu-id="3c9a4-103">Color Fonts</span></span>

<span data-ttu-id="3c9a4-104">Este tópico descreve as fontes de cor, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="3c9a4-105">Este documento contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="3c9a4-106">O que são fontes coloridas?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="3c9a4-107">Por que usar fontes de cores?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="3c9a4-108">A quais tipos de fontes de cores o Windows dá suporte?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="3c9a4-109">Usando fontes de cores</span><span class="sxs-lookup"><span data-stu-id="3c9a4-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="3c9a4-110">Usando fontes de cores em um aplicativo XAML</span><span class="sxs-lookup"><span data-stu-id="3c9a4-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="3c9a4-111">Usando fontes de cores no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9a4-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="3c9a4-112">Usando fontes de cores com DirectWrite e Direct2D</span><span class="sxs-lookup"><span data-stu-id="3c9a4-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="3c9a4-113">Usando fontes de cores com Win2D</span><span class="sxs-lookup"><span data-stu-id="3c9a4-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="3c9a4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c9a4-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="3c9a4-115">O que são fontes coloridas?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-115">What are color fonts?</span></span>

<span data-ttu-id="3c9a4-116">Fontes de cores, também conhecidas como fontes com várias cores ou fontes de desvio, são uma tecnologia de fonte que permite que os designers de fontes usem diversas cores dentro de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="3c9a4-117">Fontes de cores permitem cenários de texto multicolorido em aplicativos e sites com menos código e suporte a sistemas operacionais mais robustos do que as técnicas ad hoc implementadas acima do sistema de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="3c9a4-118">As fontes às quais você provavelmente está mais familiarizado não são fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="3c9a4-119">Essas fontes definem apenas a forma dos glifos que elas contêm, com contornos vetoriais ou bitmaps monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="3c9a4-120">No momento do desenho, um processador de texto preenche a forma de glifo usando uma única cor (a cor da fonte) especificada pelo aplicativo ou documento que está sendo renderizado.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="3c9a4-121">As fontes de cores, por outro lado, contêm informações de cores além das informações de forma.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="3c9a4-122">Algumas abordagens permitem que os designers de fontes ofereçam várias paletas de cores, dando a fonte de cor a flexibilidade artística.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="3c9a4-123">O exemplo a seguir mostra um glifo da fonte de cor do Segoe UI Emoji.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="3c9a4-124">O glifo é renderizado no monocromático à esquerda e colorido à direita.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Mostra glifos lado a lado, o glifo esquerdo renderizado em monocromático, o direito na fonte de cores Segoe U de Emoji.](images/color-font-cat.png)

<span data-ttu-id="3c9a4-126">As fontes de cores normalmente incluem informações de fallback para plataformas que não dão suporte a fontes de cores ou para cenários em que a funcionalidade de cores foi desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="3c9a4-127">Nessas plataformas, as fontes de cores são renderizadas como fontes monodesvios regulares.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="3c9a4-128">Por que usar fontes de cores?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-128">Why use color fonts?</span></span>

<span data-ttu-id="3c9a4-129">Historicamente, designers e desenvolvedores usaram uma variedade de técnicas para obter texto multicolorido.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="3c9a4-130">Por exemplo, os sites geralmente usam imagens rasterizadas em vez de texto para exibir cabeçalhos ricos.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="3c9a4-131">Essa abordagem habilita a flexibilidade artística, mas os gráficos rasterizados não são bem dimensionados para todos os tamanhos de exibição, nem fornecem os mesmos recursos de acessibilidade que o texto real.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="3c9a4-132">Outra técnica comum é sobreposição de várias fontes monocromáticas em diferentes cores de fonte, mas isso normalmente requer um código de layout extra para gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="3c9a4-133">Fontes de cores oferecem uma maneira de atingir esses efeitos visuais com toda a simplicidade e funcionalidade de fontes regulares.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="3c9a4-134">O texto renderizado em uma fonte de cor é igual a outro texto: pode ser copiado e colado, pode ser analisado por ferramentas de acessibilidade e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="3c9a4-135">A quais tipos de fontes de cores o Windows dá suporte?</span><span class="sxs-lookup"><span data-stu-id="3c9a4-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="3c9a4-136">A [especificação OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) define várias maneiras de inserir informações de cor em uma fonte.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="3c9a4-137">A partir da atualização de aniversário do Windows 10, DirectWrite e Direct2D (e as estruturas do Windows criadas neles) dão suporte a todas essas abordagens.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="3c9a4-138">Eles são resumidos na tabela abaixo:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="3c9a4-139">Técnica</span><span class="sxs-lookup"><span data-stu-id="3c9a4-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="3c9a4-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c9a4-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9a4-141">[COLR](/typography/opentype/spec/colr) / Tabelas [Cpal](/typography/opentype/spec/cpal)</span><span class="sxs-lookup"><span data-stu-id="3c9a4-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="3c9a4-142">Usa camadas de vetores coloridos, cujas formas são definidas da mesma maneira que os contornos de glifo de cor única.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="3c9a4-143">**Observação:** Com suporte a partir do Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="3c9a4-144">Tabela [SVG](/typography/opentype/spec/svg)</span><span class="sxs-lookup"><span data-stu-id="3c9a4-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="3c9a4-145">Usa imagens vetoriais criadas no formato gráfico de vetor escalonável.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="3c9a4-146">**Observação:** A partir da atualização de aniversário do Windows 10, o DirectWrite dá suporte a um subconjunto da especificação SVG completa. Nem todo conteúdo SVG é garantido para renderizar em uma fonte de SVG OpenType.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="3c9a4-147">Consulte [suporte a SVG](../direct2d/svg-support.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="3c9a4-148">[CBDT](/typography/opentype/spec/cbdt) / Tabelas [CBLC](/typography/opentype/spec/cblc)</span><span class="sxs-lookup"><span data-stu-id="3c9a4-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="3c9a4-149">Usa imagens de bitmap de cores inseridas.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3c9a4-150">tabela [sbix](/typography/opentype/spec/sbix)</span><span class="sxs-lookup"><span data-stu-id="3c9a4-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="3c9a4-151">Usa imagens de bitmap de cores inseridas.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="3c9a4-152">Usando fontes de cores</span><span class="sxs-lookup"><span data-stu-id="3c9a4-152">Using color fonts</span></span>

<span data-ttu-id="3c9a4-153">Da perspectiva do usuário, as fontes de cor são apenas fontes.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="3c9a4-154">Por exemplo, eles normalmente podem ser instalados e desinstalados do sistema da mesma forma que as fontes monocromáticas e são renderizados como texto comum e selecionável.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="3c9a4-155">Da perspectiva do Developer s também, as fontes de cores geralmente são usadas da mesma maneira que as fontes monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="3c9a4-156">Nas estruturas XAML e Microsoft Edge, você pode estilizar o texto com fontes de cores da mesma maneira que as fontes regulares e, por padrão, o texto será renderizado em cores.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="3c9a4-157">No entanto, se seu aplicativo chama diretamente APIs Direct2D (ou APIs Win2D) para renderizar o texto, ele deve solicitar explicitamente a renderização de fonte de cor.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="3c9a4-158">Usando fontes de cores em um aplicativo XAML</span><span class="sxs-lookup"><span data-stu-id="3c9a4-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="3c9a4-159">Os elementos de texto da plataforma XAML (como [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) dão suporte a fontes de cores por padrão.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="3c9a4-160">Basta estilizar o texto com uma fonte de cor e todos os glifos de cor serão renderizados em cores.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="3c9a4-161">O exemplo de código a seguir mostra uma maneira de estilizar um TextBlock com uma fonte de cor empacotada com seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="3c9a4-162">A mesma técnica se aplica a fontes regulares.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="3c9a4-163">Se você nunca quiser que seu elemento de texto XAML processe texto multicolorido, defina sua propriedade [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) como false.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="3c9a4-164">Usando fontes de cores no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9a4-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="3c9a4-165">As fontes de cores são renderizadas por padrão em sites e aplicativos Web em execução no Microsoft Edge, incluindo o controle [WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="3c9a4-166">Basta usar HTML e CSS para estilizar o texto com uma fonte de cor e todos os glifos de cor serão renderizados em cores.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="3c9a4-167">Usando fontes de cores com DirectWrite e Direct2D</span><span class="sxs-lookup"><span data-stu-id="3c9a4-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="3c9a4-168">Seu aplicativo pode usar os métodos de desenho de texto de nível superior do Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) ou pode usar técnicas de nível inferior para desenhar diretamente os glifos.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="3c9a4-169">Em ambos os casos, seu aplicativo requer alterações de código para manipular os glifos de cor corretamente.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="3c9a4-170">Se seu aplicativo usar Direct2D de **DrawText** e APIs **DrawTextLayout** , observe que eles não renderizam glifos de cor por padrão.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="3c9a4-171">Isso é para evitar alterações de comportamento inesperadas em aplicativos de renderização de texto que foram criados antes do suporte à fonte de cores.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="3c9a4-172">Para aceitar a renderização de glifo de cor, passe o sinalizador [**Opções de texto de desenho d2d1 habilitar opções de \_ \_ \_ \_ \_ \_ fonte de cor**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) para o método de desenho.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="3c9a4-173">O exemplo de código a seguir mostra como chamar o método DrawText Direct2D s para renderizar uma cadeia de caracteres em uma fonte de cor:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



<span data-ttu-id="3c9a4-174">Se seu aplicativo usa APIs de nível inferior para manipular as execuções de glifos diretamente, ele continuará a funcionar na presença de fontes de cores, mas não poderá desenhar glifos de cor sem lógica adicional.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="3c9a4-175">Para lidar corretamente com os glifos de cor, seu aplicativo deve:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="3c9a4-176">Passe as informações de execução de glifo para [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), juntamente com um parâmetro de [**formatos de \_ \_ imagem \_ de glifo DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica que tipo (s) de glifo de cor o aplicativo está preparado para lidar.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="3c9a4-177">Se quaisquer glifos de cor estiverem presentes (com base na fonte e nos **\_ formatos de \_ imagem \_ de glifo DWRITE** solicitados), DirectWrite dividirá a execução do glifo primário em execuções de glifos de cores individuais que podem ser acessadas por meio do objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) retornado na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="3c9a4-178">Verifique o HRESULT retornado por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar se as execuções de glifo de cor foram detectadas.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="3c9a4-179">Um **HRESULT** de **DWRITE \_ E \_ nocolor** indica nenhuma execução de glifo de cor aplicável.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="3c9a4-180">Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) não reportou nenhuma execução de glifo de cor (retornando **DWRITE \_ E \_ nocolor**), a execução de glifo inteira será tratada como monodesvio e seu aplicativo deverá desenhá-lo conforme desejado (por exemplo, usando [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="3c9a4-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="3c9a4-181">Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reportar a presença de execuções de glifo de cor, seu aplicativo deverá ignorar a execução de glifo primário e, em vez disso, usar as execuções de glifo de cor retornadas por TranslateColorGlyphRun.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="3c9a4-182">Para fazer isso, itere o objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) retornado, recuperando cada execução de glifo de cor e desenhando-o conforme apropriado para seu formato de imagem de glifo (por exemplo, você pode usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para desenhar glifos de bitmap de cor e glifos SVG, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="3c9a4-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="3c9a4-183">O exemplo de código a seguir mostra a estrutura geral deste procedimento:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-183">The following code example shows the general structure of this procedure:</span></span>


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="3c9a4-184">Usando fontes de cores com Win2D</span><span class="sxs-lookup"><span data-stu-id="3c9a4-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="3c9a4-185">Semelhante ao Direct2D, as APIs de desenho de texto do Win2D não renderizam glifos de cores por padrão.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="3c9a4-186">Para aceitar a renderização de glifo de cor, defina o sinalizador de opções [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) no objeto de formato de texto que seu aplicativo passa para o método de desenho de texto.</span><span class="sxs-lookup"><span data-stu-id="3c9a4-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="3c9a4-187">O exemplo de código a seguir mostra como renderizar uma cadeia de caracteres em uma fonte de cor usando Win2D:</span><span class="sxs-lookup"><span data-stu-id="3c9a4-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a><span data-ttu-id="3c9a4-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c9a4-188">Related topics</span></span>

[<span data-ttu-id="3c9a4-189">Exemplo de glifo colorido DirectWrite</span><span class="sxs-lookup"><span data-stu-id="3c9a4-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="3c9a4-190">**Interface IDWriteFontFace4**</span><span class="sxs-lookup"><span data-stu-id="3c9a4-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="3c9a4-191">**Método IDWriteFactory4:: TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="3c9a4-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="3c9a4-192">**ID2D1DeviceContext4: método rawText de:D**</span><span class="sxs-lookup"><span data-stu-id="3c9a4-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

