---
title: O que há de novo no DirectWrite
description: Aqui estão algumas das novas adições ao DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: bf1a62917e18dcda7e7c4e3f1b05731b60628967
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2020
ms.locfileid: "103644196"
---
# <a name="whats-new-in-directwrite"></a>O que há de novo no DirectWrite

Este tópico descreve o que há de novo no [DirectWrite](direct-write-portal.md) para várias versões do Windows 10.

## <a name="project-reunion-01-prerelease"></a>Versão de pré-lançamento do Project reunião 0,1

A [reunião do projeto](/windows/apps/project-reunion/) apresenta uma nova versão do DirectWrite, chamada DWriteCore, que é executada em versões do Windows até o Windows 8 e abre a porta para você usá-la entre plataformas. Para obter mais detalhes, consulte [visão geral do DWriteCore](dwritecore-overview.md).

## <a name="windows-10-may-2019-update"></a>Atualização de maio de 2019 para Windows 10

Nenhum recurso ou API foi adicionado nem atualizado para o Windows 10, versão 1903 (10,0; Build 18362) &mdash; também conhecido como Windows 10 pode 2019 atualização.

## <a name="windows-10-october-2018-update"></a>Atualização de outubro de 2018 para o Windows 10

Os seguintes recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1809 (10,0; Build 17763) &mdash; também conhecido como atualização do Windows 10 de outubro de 2018.

### <a name="new"></a>Novo

- Enumeração de [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type)
- Interface [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) e seus métodos

## <a name="windows-10-april-2018-update"></a>Atualização de abril de 2018 do Windows 10

Os seguintes recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1803 (10,0; Build 17134) &mdash; também conhecido como atualização do Windows 10 de abril de 2018.

### <a name="new"></a>Novo

- Interface [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) e seus métodos
- Interface [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) e seus métodos
- Interface [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) e seus métodos

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Os seguintes recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1709 (10,0; Build 16299) &mdash; também conhecido como atualização dos criadores de outono do Windows 10.

### <a name="new"></a>Novo

- Enumeração de [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes)
- Enumeração de [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes)
- Enumeração de [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)
- Enumeração de [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model)
- Interface [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) e seus métodos
- Interface [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) e seus métodos
- Interface [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) e seus métodos
- Interface [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) e seus métodos
- Interface [**IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) e seus métodos
- Interface [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) e seus métodos
- Interface [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) e seus métodos
- Interface [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) e seus métodos
- Interface [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) e seus métodos
- Interface [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) e seus métodos
- Interface [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) e seus métodos
- Interface [**IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) e seus métodos
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) macro
- Estrutura de [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
- Estrutura de [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)

### <a name="moved"></a>Sido

A enumeração de [**DWRITE_GLYPH_IMAGE_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) movida de `dwrite_3.h` para `dcommon.h` .

## <a name="windows-10-creators-update"></a>Atualização do Windows 10 para Criadores

Os seguintes recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1703 (10,0; Build 15063) &mdash; também conhecido como atualização do Windows 10 para criadores.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Suporte expandido à API para fontes de nuvem e conjuntos de fontes personalizadas

As APIs incluídas no Windows 10 permitem que os aplicativos acessem facilmente fontes de um serviço de fontes do Windows. Na atualização do Windows 10 para criadores, as APIs para fontes remotas são estendidas para permitir o acesso fácil a fontes de outras fontes na Web que podem ser acessadas usando HTTP ou HTTPS. 

As novas APIs de fonte remota podem ser usadas com serviços Web públicos ou privados. Além disso, eles podem ser usados para acessar arquivos de fontes brutos, OpenType (. ttf,. otf.,. TTC,. OTC) ou fontes empacotadas nos formatos de contêiner [WOFF](https://www.w3.org/TR/WOFF/) ou [WOFF2](https://www.w3.org/TR/WOFF2/) . As novas APIs são usadas em conjunto com as APIs existentes para enfileirar solicitações para baixar dados de fonte remoto e para manipular o processo de download real.

Outras novas APIs facilitam para os aplicativos trabalhar com fontes personalizadas armazenadas no sistema de arquivos local ou que são carregadas em um buffer de memória.

Para obter mais informações sobre novas APIs para trabalhar com fontes remotas, conjuntos de fontes personalizadas ou formatos de contêiner WOFF/WOFF2, consulte o seguinte tópico:

[Conjuntos de fontes personalizados](custom-font-sets-win10.md)

Consulte também os links para tópicos de referência de API fornecidos nesse tópico.  O uso de APIs novas e existentes para trabalhar com fontes personalizadas também é ilustrado no [exemplo de conjuntos de fontes personalizadas DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Este exemplo ilustra a implementação de código para vários cenários diferentes, incluindo fontes locais em disco, fontes remotas na Web, dados de fonte na memória e fontes nos formatos WOFF ou WOFF2 empacotados.

### <a name="initial-support-for-opentype-font-variations"></a>Suporte inicial para variações de fontes OpenType

A versão 1,8 da especificação de formato de fonte OpenType introduziu uma nova extensão empolgante para o formato conhecido como variações de fontes OpenType. O DirectWrite foi atualizado na atualização do Windows 10 para criadores para dar suporte a instâncias nomeadas de fontes de variáveis. Para obter mais informações, consulte o tópico a seguir:

[Fontes variáveis OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Atualização de Aniversário do Windows 10

Os seguintes recursos e APIs foram adicionados ou atualizados para o Windows 10, versão 1607 (10,0; Build 14393) &mdash; também conhecido como atualização de aniversário do Windows 10.

### <a name="improved-support-for-color-fonts"></a>Suporte aprimorado para fontes coloridas

A partir da atualização de aniversário do Windows 10, o DirectWrite fornece suporte interno para uma variedade maior de formatos de fonte de cor, permitindo que os desenvolvedores usem mais tipos de fontes em seus aplicativos com DirectWrite do que nunca. Isso inclui suporte para:

-   A tabela OpenType ' COLR ', que habilita o conteúdo de vetor compacto em fontes. (Com suporte desde Windows 8.1.)
-   A tabela OpenType ' SVG ', que habilita o conteúdo SVG em fontes.
-   A tabela OpenType ' CBDT ', que permite o conteúdo de bitmap em cores em fontes.
-   A tabela OpenType ' sbix ', que permite o conteúdo de bitmap em cores em fontes.

[Direct2D](../direct2d/direct2d-portal.md), que usa DirectWrite para a renderização de texto, oferece suporte a esses formatos de fonte de cor automaticamente quando o sinalizador de fontes de texto de desenho de d2d1 habilitação de [**\_ \_ \_ \_ \_ cor \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) é habilitado. Para mais informações, consulte os seguintes tópicos:

-   [Fontes de cores](color-fonts.md)
-   [Exemplo de glifo de cor de DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Suporte para Adobe Typekit e outros clientes de serviço de fonte

Alguns serviços de fontes, como o Adobe Typekit, têm utilitários do lado do cliente que permitem a um usuário carregar fontes do serviço e usá-las em diferentes aplicativos em seu computador Windows. Normalmente, esses utilitários funcionam fazendo chamadas de tempo de execução para o GDI para carregar fontes adicionais, em vez de instalar permanentemente as fontes no sistema. Por causa desse design, em versões anteriores do Windows, as fontes seriam utilizáveis em aplicativos baseados em GDI, mas não em aplicativos DirectWrite. A partir da atualização de aniversário do Windows 10, as fontes que são carregadas por tais utilitários também estarão disponíveis em DirectWrite, bem como em GDI.

As fontes carregadas por um utilitário de serviço de fonte são visíveis na coleção de fontes do sistema obtida chamando o método [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Como os serviços de fonte geralmente seguem um modelo de licenciamento por usuário, as fontes carregadas por esses utilitários são gerenciadas por usuário. Como resultado, os aplicativos DirectWrite existentes podem utilizar fontes que os usuários finais obtiveram usando tais serviços, sem nenhuma alteração de código necessária no aplicativo, fornecendo uma experiência mais direta aos usuários.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Suporte para coleções OpenType usando contornos CFF

Os formatos de fonte OpenType e TrueType têm suporte longo para a capacidade de várias fontes serem empacotadas juntas em um único arquivo de fonte, conhecido como "coleção de fontes". A especificação OpenType sempre permitiu que as fontes utilizassem formatos TrueType ou CFF para dados de estrutura de tópicos de glifo. Até recentemente, no entanto, a especificação só é permitida para coleções nas quais os contornos de glifos usam o formato TrueType. A versão 1,7 do OpenType agora permite que as coleções usem formatos TrueType ou CFF para dados de estrutura de tópicos de glifo. A partir da atualização de aniversário do Windows 10, o DirectWrite dará suporte a coleções OpenType usando dados de estrutura de tópicos do CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Integração do serviço de fontes do Windows

A partir do Windows 10, as fontes incluídas com o Windows estão disponíveis em um serviço online e podem ser acessadas por meio do DirectWrite em qualquer dispositivo Windows 10. Isso se aplica a todas as edições do Windows 10, incluindo Windows 10 Mobile, Xbox e HoloLens, bem como o cliente de desktop. Isso permite que os aplicativos exibam conteúdo usando qualquer fonte do Windows, mesmo que a fonte não esteja instalada atualmente no dispositivo.

O suporte para os mecanismos de serviço de fonte DirectWrite foi implementado na estrutura XAML, o que significa que todos os aplicativos que usam XAML não exigem nenhuma alteração de código para aproveitar o serviço de fonte. O [exemplo de código de fontes baixáveis (XAML)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) demonstra isso. Aplicativos que chamam APIs DirectWrite diretamente precisarão usar novas APIs para usar os mecanismos de serviço de fonte. Para mais informações, consulte os seguintes tópicos:

-   Método [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection)
-   Interface [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   Interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

O [exemplo de código de fontes baixáveis (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) ilustra o uso de várias das novas APIs.

### <a name="font-set-apis"></a>APIs de conjunto de fontes

As interfaces de coleção de fontes do DirectWrite fornecem uma exibição para uma coleção de fontes organizadas por famílias de fontes, usando peso, ampliação e estilo como atributos de subfamília. Internamente, o DirectWrite implementa a interface de coleção de fontes usando uma lista simples de fontes com vários atributos. Essa abordagem é mais flexível, pois o no pode dar suporte à enumeração de famílias de peso/alongamento/estilo, mas também pode oferecer suporte à consulta e filtragem usando outros atributos de fonte também.

No Windows 10, esse mecanismo mais flexível de manipulação de fontes é disponibilizado para aplicativos por meio do IDWriteFontSet e das APIs relacionadas. As APIs do conjunto de fontes podem ser usadas, por exemplo, para criar uma interface do usuário personalizada do seletor de fonte, aproveitando as propriedades de fonte personalizadas do aplicativo em um conjunto de fontes personalizado.

Para mais informações, consulte os seguintes tópicos:

-   Interface [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ Enumeração \_ de \_ ID de propriedade de fonte**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   Método [**IDWriteFontFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset)

### <a name="new-text-layout-line-spacing-modes"></a>Novos modos de espaçamento de linha de layout de texto

As interfaces de layout de texto e de formato de texto do DirectWrite dão suporte a novos modos de espaçamento de linha. Em versões anteriores, a implementação de layout de texto do DirectWrite é permitida para o espaçamento de linha no qual a altura de cada linha foi definida automaticamente com base no item mais alto dentro de uma linha (o modo "padrão") ou o espaçamento de linha com todas as linhas definidas como uma altura uniforme determinada pelo aplicativo (o modo "uniforme"). No Windows 10, há suporte para um modo adicional de espaçamento de linha "proporcional" que oferece aos aplicativos mais opções de comportamento de espaçamento de linha. Para mais informações, consulte os seguintes tópicos:

-   Interface [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Método [**IDWriteTextLayout3:: SetLineSpacing**](idwritetextlayout3-setlinespacing.md)
-   [**DWRITE \_ Estrutura de \_ espaçamento de linha**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ Enumeração \_ do \_ método de espaçamento de linha**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ Enumeração \_ de \_ \_ uso de lacuna de linha de fonte**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   Método [**IDWriteTextLayout3:: GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)
-   [**DWRITE \_ Estrutura de \_ METRICS1 de linha**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

O [exemplo de código de espaçamento de linha (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) ilustra o uso de várias das novas APIs e também fornece uma visualização de todos os diferentes modos de espaçamento de linha que tornam muito mais fácil entender as várias opções de espaçamento de linha disponíveis.

### <a name="gdi-interop"></a>Interoperabilidade GDI

Desde sua introdução no Windows 7, o DirectWrite forneceu um caminho de migração para aplicativos que foram originalmente implementados usando o modelo de fonte, o layout de texto e a renderização da GDI. Isso foi fornecido por meio da \[ \[ \] \] interface IDWriteGdiInterop. No Windows 10, as APIs adicionais fornecem recursos adicionais de interoperabilidade GDI. Para obter informações adicionais, consulte o seguinte tópico:

-   Interface [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Renderizando fontes de cores

A partir do Windows Windows 8.1, o DirectWrite fornece suporte para fontes de cores. [Direct2D](../direct2d/direct2d-portal.md), que usa DirectWrite para a renderização de texto, adicionou o valor de enumeração d2d1 \_ \_ Opções de texto de desenho \_ \_ habilitar \_ \_ fonte de cor para habilitar esse recurso ao desenhar o texto. Para mais informações, consulte os seguintes tópicos:

-   [**D2d1 \_ Enumeração \_ de \_ Opções de texto de desenho**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   Método [**IDWriteFactory2:: TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)

## <a name="windows-8"></a>Windows 8

Uma nova interface de fábrica, [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1), para a criação de interfaces adicionais que estão disponíveis.

Propriedades de fonte adicionais, como: super/subscrito, inclinação do cursor, PANOse e intervalos Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Melhorias de espaçamento, como: espaçamento de caracteres de controle, pares de kerning herdados e justificação. Consulte o tópico [justificativa, kerning e espaçamento](justification--kerning--and-spacing.md) para obter mais informações.

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Parâmetros e destinos de renderização aprimorados.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Melhorias na análise de complexidade de texto.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Novas propriedades de script, novo suporte a scripts (Unicode 6), adições de fallback de fonte, parênteses emparelhados e aumento bidirecional.

Aprimoramentos de desempenho do cache de fontes. A partir do Windows 8, o cache de fontes é global e é iniciado quando o computador é inicializado.

Novos modos de renderização.

A partir do Windows 8, o [DirectWrite](direct-write-portal.md) dá suporte a vários recursos que ajudam você a fazer aplicativos para o mercado mundial.

Aqui estão várias áreas que ajudam você a implementar aplicativos de Rich Text que podem ser adaptados aos clientes em todo o mundo.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Extensões do chinês, japonês e coreano C & D

A cada poucos anos, o consórcio Unicode lança uma lista padronizada de inclusões em chinês, japonês e coreano bloco de ideograma. Com a revisão de Unicode 6,0, eles lançaram os blocos de extensão C e D. Esses blocos de ideogramas podem ser encontrados na extensão de site Unicode [C](https://www.unicode.org/charts/PDF/U2A700.pdf) e na [extensão D](https://www.unicode.org/charts/PDF/U2B740.pdf).

A partir do Windows 8, o [DirectWrite](direct-write-portal.md) dá suporte ao íntegra Unicode para esses novos blocos de ideogramas CJK padronizadas, para que você possa usá-los em aplicativos DirectWrite.

### <a name="indian-rupee-symbol"></a>Símbolo de Rúpia Indiana

Em março de 2005, o governo Índico anunciou uma competição para escolher um símbolo para a moeda de Rúpia indiana. Após muita competição, no dia 15 de julho de 2010, o governo Índico escolheu o design criado por D. Udaya Kumar e o [DirectWrite](direct-write-portal.md) inclui suporte para o ponto Unicode vinculado ao símbolo. Assim, os aplicativos DirectWrite agora dão suporte a esse símbolo de moeda.

### <a name="emoji"></a>Emoji

O [DirectWrite](direct-write-portal.md) agora dá suporte ao uso de Emoji em aplicativos. Versões anteriores do DirectWrite, apresentadas com uma caixa de glifo ausente se você tentar renderizar um ideogram de Emoji. A partir do Windows 8, o DirectWrite dá suporte ao CodeBlock Unicode associado ao Emoji, portanto, se seu aplicativo usar o íntegra padrão Unicode para Emoji, ele exibirá os glifos apropriados.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Idiomas birmanês, Tiffinagh e Hangul antigos

A partir do Windows 8, o [DirectWrite](direct-write-portal.md) dá suporte ao bloco de íntegra Unicode que correspondem aos glifos em Myanmar, Tiffinagh e linguagens Hangul antigas, para que você possa criar aplicativos que incluam texto desses três idiomas. Além de dar suporte a esses caracteres, o DirectWrite dá suporte à maneira única com que o Hangul antigo lida com a quebra de linha.

### <a name="new-scripts"></a>Novos scripts

A partir do Windows 8, o método [**Getscriptproperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) retorna informações para vários novos scripts. Aqui está a lista de scripts que o [DirectWrite](direct-write-portal.md) dá suporte no Windows 8 e posterior.

-   Avestan
-   Bamum
-   Batak
-   Brahmi
-   Egípcio hieroglyphics
-   Imperial Armi
-   Inscriptional Pahlavi
-   Inscriptional Parthian
-   Javanês
-   Kaithi
-   Lisu (Fraser)
-   Mandaica
-   Meetei Mayek
-   Árabe antigo Sul
-   Turco antigo (Orkhon)
-   Samaritan
-   Tai Tham (Lanna)
-   Tai Viet