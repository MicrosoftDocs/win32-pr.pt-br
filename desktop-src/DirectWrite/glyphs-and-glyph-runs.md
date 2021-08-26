---
title: Glifos e execuções de glifo
description: os glifos e as execuções de glifo estão disponíveis na camada mais baixa de funcionalidade da API DirectWrite, na camada de renderização de glifo.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite, glifos
- DirectWrite, execuções de glifo
- execuções de glifo
- glifos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902906"
---
# <a name="glyphs-and-glyph-runs"></a>Glifos e execuções de glifo

os glifos e as execuções de glifo estão disponíveis na camada mais baixa de funcionalidade da API [DirectWrite](direct-write-portal.md) , na camada de renderização de glifo.

## <a name="glyphs"></a>Glifos

Um glifo é uma representação física de um caractere em uma determinada fonte. Os caracteres podem ter muitos glifos, com cada fonte em um sistema potencialmente definindo um glifo diferente para esse caractere.

Dois ou mais glifos também podem ser combinados em um único glifo, esse processo é chamado de composição de glifo. Isso também pode ser feito na direção oposta, um único glifo sendo dividido em vários glifos, conhecido como decomposição de glifo.

### <a name="alternate-glyphs"></a>Glifos alternativos

As fontes podem fornecer glifos alternativos para caracteres, como os glifos alternativos estilísticos para a fonte OpenType Pericles, conforme mostrado na captura de tela a seguir. Os caracteres ' A ', ' E ' e ' O ' são renderizados com glifos alternativos estilísticos.

![captura de tela de "Green Mythology antigo", com "a", "e" e "o" usando glifos alternativos](images/opentypealternateglyphs.png)

Outro exemplo de glifos alternativos são glifos de traços violentos. A captura de tela a seguir mostra os glifos padrão e Swash para a fonte Pescadero.

![captura de tela das letras "a" por meio de "n" em glifos padrão e Swash](images/opentypeswashstandard.png)

Traços violentos e outros recursos tipográficos, incluindo glifos alternativos mais elaborados, estão disponíveis por meio de [OpenType](../intl/opentype-font-format.md). Recursos tipográficos OpenType podem ser aplicados a um intervalo de texto usando o [**IDWriteTextLayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando a constante de enumeração de [**marca de \_ \_ recurso \_ de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) associada ao recurso desejado.

## <a name="glyph-runs"></a>Execuções de glifo

Uma execução de glifo representa um conjunto contíguo de glifos que têm a mesma face e tamanho de fonte, bem como o mesmo efeito de desenho de cliente, se houver. Sublinhado e tachado não fazem parte da execução de glifos para o intervalo de texto ao qual são aplicadas e são desenhados posteriormente. Objetos embutidos, como imagens, também são desenhados separadamente, pois não fazem parte de uma fonte.

### <a name="the-idwritefontface-interface"></a>A interface IDWriteFontFace

[DirectWrite](direct-write-portal.md) usa o mesmo sistema para classificação de fontes como Windows o WPF (Pesentation Foundation), de modo que pode haver várias fontes físicas por cada família de fontes. uma face de fonte, como a interface [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) na DirectWrite, representa uma fonte física, com um peso específico, uma inclinação e uma ampliação. Ele contém o tipo de face da fonte, as referências de arquivo apropriadas, os dados de identificação facial e vários dados de fonte, como métricas, nomes e contornos de glifos.

O [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) pode ser criado diretamente a partir de um nome de fonte ou obtido de uma coleção de fontes.

### <a name="glyph-metrics"></a>Métricas de glifo

Os glifos individuais têm métricas associadas a eles. Você pode obter as métricas para todos os glifos em uma execução de glifo usando o método [**IDWriteFontFace:: GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) . Isso retorna uma estrutura de [**\_ \_ métricas de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) que tem a largura antecipada, a extremidade esquerda e direita, as partes superior e inferior, a altura e a origem da linha de base vertical.

O diagrama a seguir mostra várias métricas de dois caracteres de glifo diferentes.

![diagrama das métricas de dois glifos diferentes](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Desenhando uma execução de glifo

Ao implementar um processador de texto personalizado, a renderização de glifos é manipulada pelo [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), um método de retorno de chamada que você implementa como parte de uma classe derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). A estrutura de [**\_ \_ execução de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que é passada para [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contém um objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , chamado *fontface*, que representa a face da fonte para toda a execução do glifo.

O objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) também fornece o método [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , que computa os contornos de glifos usando um retorno de chamada de coletor de geometria especificado, como [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ao renderizar com [Direct2D](../direct2d/direct2d-portal.md).

Para obter mais informações, consulte o tópico [como implementar um processador de texto personalizado](how-to-implement-a-custom-text-renderer.md) .

 

 