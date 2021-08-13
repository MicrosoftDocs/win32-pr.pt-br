---
title: Métricas de texto
description: para auxiliar o layout, a seleção de fontes personalizada e outras operações com uso intensivo de métrica, a partir do Windows 8, DirectWrite tem várias novas APIs para expressar todas as informações sobre as fontes que você pode precisar para desenvolver aplicativos de rich text.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e5c5eecce93eac3726195410cf5b215bd65de3d7e48248a68d6d96858f8fed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329236"
---
# <a name="text-metrics"></a>Métricas de texto

para auxiliar o layout, a seleção de fontes personalizada e outras operações com uso intensivo de métrica, a partir do Windows 8, [DirectWrite](direct-write-portal.md) tem várias novas APIs para expressar todas as informações sobre as fontes que você pode precisar para desenvolver aplicativos de rich text.

## <a name="panose"></a>PANOSE

O PANOse é um sistema de classificação visual para identificar tipos. A classificação PANOse contém informações sobre a família, estilo de serif, peso, proporção, contraste, traço, estilo ARM, altura X etc. Esta informação descreve o estilo visual da fonte. Essas informações são importantes porque as fontes com valores PANOse semelhantes parecem semelhantes. Isso é muito útil em situações em que uma fonte não está disponível e o aplicativo precisa fazer fallback para uma fonte que está disponível. Comparar os valores de PANOse para fontes permite que você escolha uma fonte semelhante visualmente à fonte original.

Para acessar as informações de PANOse para uma fonte, use o método [**Getpanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) nas interfaces [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) e [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) . Esse método retorna uma [**enumeração \_ Panose DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) que contém todas as informações de Panose para essa fonte.

## <a name="additional-metrics"></a>Métricas adicionais

a partir do Windows 8, a API do [DirectWrite](direct-write-portal.md) também dá suporte a várias métricas novas para expressar informações úteis sobre as fontes para seu aplicativo. Essas novas métricas incluem essas informações.

-   Métricas da caixa delimitadora de glifos esquerda, direita, superior e inferior.
-   Posicionamento X e Y para elementos sobrescrito e subscrito.
-   Informações de dimensionamento X e Y para elementos sobrescrito e subscrito.
-   Se a fonte tem métricas tipográficas ou não.

Essas informações estão disponíveis por meio do novo método [**Getmetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) nas interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) . Esse método retorna uma estrutura de [**\_ \_ METRICS1 de fonte DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) que contém todas essas informações.

## <a name="caret-metrics"></a>Métricas de cursor

Para criar aplicativos de edição de texto, você precisa acessar informações sobre como desenhar o cursor que navega pelo texto. a partir do Windows 8, [DirectWrite](direct-write-portal.md) fornece o método [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) nas interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) para esse cenário. **GetCaretMetrics** retorna uma enumeração de [**\_ \_ métricas de cursor DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) que contém informações sobre a inclinação e o deslocamento do cursor ao longo da linha de base.

Essas informações serão especialmente úteis se você quiser ter a inclinação do cursor apropriadamente com texto em itálico.

## <a name="monospaced-discoverability"></a>Descoberta monoespaçada

Os aplicativos que permitem que os usuários gravem o código do computador geralmente usam fontes com espaçamento uniforme no lugar de fontes mais tradicionais. portanto, você pode ter mais controle sobre a seleção de fontes em aplicativos relacionados ao desenvolvimento, [DirectWrite](direct-write-portal.md) expressa se uma fonte tem ou não espaçamento uniforme por meio da API. O método [**IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) na interface [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) retorna um booliano que indica se a fonte tem ou não espaçamento uniforme.

## <a name="font-name-matching"></a>Correspondência de nome de fonte

Aplicativos de Rich Text como leitores de PDF precisam ser capazes de corresponder fontes em seu conteúdo a fontes no sistema, precisam de acesso a nomes completos de fontes em vários formatos. portanto, você pode corresponder melhor as fontes, [DirectWrite](direct-write-portal.md) contém uma enumeração que expressa informações de nomenclatura completas sobre uma fonte em muitos formatos.

você usa a enumeração de [**\_ ID de cadeia de \_ caracteres \_ informativa DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) para obter o nome completo, PostScript nome e PostScript nome CID de qualquer fonte no sistema. Essas informações são valiosas quando você precisa corresponder as fontes em seu aplicativo às fontes apropriadas no sistema local.

## <a name="glyph-advances"></a>Avanços de glifo

O método **GetGlyphAdvances** nas interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) usa a contagem de glifos e os índices dos quais você precisa de informações sobre os avanços e, em seguida, retorna os avanços dos glifos em questão.

## <a name="unicode-ranges"></a>Intervalos Unicode

Os aplicativos que desejam manipular sua própria seleção de fonte precisam de acesso aos intervalos Unicode com suporte da fonte. Dessa forma, se uma ponto Unicode não tiver suporte da fonte, o aplicativo poderá escolher uma fonte apropriada que contenha esse glifo. Sem essas informações, o aplicativo pode usar uma fonte que não contém todos os glifos necessários para exibir as informações presentes.

O método [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) nas interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) usa o número máximo de intervalos passados do cliente e retorna os intervalos reais com suporte da fonte.

## <a name="eudc-font-collection"></a>Coleção de fontes EUDC

Use o método [**GetEudcFontCollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) na interface [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) para acessar a coleção de fontes Eudc. Esse método funciona da mesma maneira que [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), mas, em vez disso, retorna um ponteiro para uma coleção de fontes Eudc.

 

 