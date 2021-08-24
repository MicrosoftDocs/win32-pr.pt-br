---
title: Texto vertical
description: A partir do Windows 8, DirectWrite tem várias novas APIs que permitem que você use texto vertical em seus aplicativos.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa5e6626ae77e610c38bfb90def7cfe068db80f7f300f58a734969fb107a46a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632535"
---
# <a name="vertical-text"></a>Texto vertical

A partir do Windows 8, [DirectWrite](direct-write-portal.md) tem várias novas APIs que permitem que você use texto vertical em seus aplicativos.

## <a name="drawing-vertical-text"></a>Desenhando texto vertical

Você pode desenhar texto vertical com Direct2D usando os [**métodos DrawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) Para desenhar o texto verticalmente, passe [**DWRITE READING DIRECTION TOP TO \_ \_ \_ \_ \_ BOTTOM**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) para o método [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) e [**DWRITE \_ FLOW DIRECTION RIGHT TO \_ \_ \_ \_ LEFT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) para o [**método IDWriteTextFormatSetFlowDirection.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) Em seguida, você pode criar e desenhar um [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vertical.

## <a name="analyzing-character-orientation"></a>Analisando a orientação de caracteres

Cada caractere tem uma orientação de caractere preferencial ou a direção em que o caractere deve ser orientado em qualquer layout direcional. Por exemplo, no layout horizontal tradicional, o texto latino e o texto chinês são orientados verticalmente. Por outro lado, em um layout vertical, o texto chinês permanece vertical e o texto latino é girado em 90 graus. Essa diferença na orientação é vista no exemplo aqui.

![uma imagem de texto em inglês e chinês em layouts horizontais e verticais.](images/vertical-text.png)

Para determinar a orientação do texto que você tem, você precisa implementar as interfaces [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) A origem e o sink levam as executações de glifo e permitem que você verifique se elas são orientadas verticalmente ou não.

Depois de implementar a origem e o sink, chame o [**método AnalyzeVerticalGlyphOrientation.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) Na imagem de exemplo, essa função retorna três executações: "Inglês", "中es" e "Inglês".

## <a name="going-from-characters-to-glyphs"></a>Ir de caracteres para glifos

Agora que você sabe que a operação contém glifos verticais, você precisa obter acesso a esses glifos. No exemplo até agora, há três executações: uma com glifos verticais e duas sem. Para fazer a transição de caracteres para glifos, chame [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Esse método retorna os índices de glifo correspondentes para os caracteres no exemplo. Como [**o método AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) retorna uma operação com glifos verticais, você precisa chamar [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), que retorna as IDs de glifo orientadas verticalmente no lugar das IDs de glifo atuais.

## <a name="drawing-text-vertically"></a>Desenhando texto verticalmente

Por fim, você precisa desenhá-lo e desenhar o texto. Como você está desenhando o texto verticalmente, precisa obter mais informações para que o texto latino seja desenhado corretamente. Se você desenhar todo o texto ao longo da linha de base central, o texto latino aparecerá flutuando no meio da linha. Você precisa de acesso à linha de base central e a Roman para alinhar o texto corretamente. Use o [**método IDWriteTextAnalyzer1::GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) para obter os valores numéricos das linhas de base especificadas. Você pode subtrair a linha de base de Roman da linha de base central para obter o deslocamento entre os dois.

Com todas essas informações, você pode desenhar o texto na tela. Primeiro, chame o [**método GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) com os resultados dos objetos [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1)

Se você estiver usando o [Direct2D](rendering-by-using-direct2d.md) também precisará definir a transformação do mundo no destino de renderização Direct2D renderização vertical.

Por fim, [**chame DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) três vezes, uma vez em cada bloco de texto. Nos dois blocos de texto que estão em inglês, você precisa aplicar o deslocamento que calculamos entre as linhas de base romes e centrais.

Agora, o texto em seu aplicativo será desenhado verticalmente, com a orientação de glifo correta.

 

 