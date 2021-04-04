---
title: Texto vertical
description: A partir do Windows 8, o DirectWrite tem uma série de novas APIs que permitem usar texto vertical em seus aplicativos.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917348"
---
# <a name="vertical-text"></a>Texto vertical

A partir do Windows 8, o [DirectWrite](direct-write-portal.md) tem uma série de novas APIs que permitem usar texto vertical em seus aplicativos.

## <a name="drawing-vertical-text"></a>Desenho de texto vertical

Você pode desenhar texto vertical com Direct2D usando os métodos [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) . Para desenhar o texto verticalmente, passe [**a \_ direção de leitura DWRITE de \_ \_ cima \_ para \_ baixo**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) até o método [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) e a [**direção do fluxo de DWRITE da \_ \_ \_ direita para a \_ \_ esquerda**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) para o método [**IDWriteTextFormatSetFlowDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) . Em seguida, você pode criar e desenhar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vertical.

## <a name="analyzing-character-orientation"></a>Analisando a orientação do caractere

Cada caractere tem uma orientação de caractere preferencial ou a direção em que o caractere deve ser orientado em qualquer layout direcional. Por exemplo, no layout horizontal tradicional, o texto latino e o texto chinês são orientados verticalmente. Por outro lado, em um layout vertical, o texto em chinês permanece vertical e o texto latino é girado 90 graus. Essa diferença na orientação é vista no exemplo aqui.

![uma imagem de texto em inglês e chinês em layouts horizontais e verticais.](images/vertical-text.png)

Para determinar a orientação do texto que você tem, você precisa implementar as interfaces [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) . A origem e o coletor assumem as execuções de glifo e permitem que você verifique se elas são orientadas verticalmente ou não.

Depois de implementar a origem e o coletor, chame o método [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) . Na imagem de exemplo, essa função retorna 3 execuções: "English", "中国" e "English".

## <a name="going-from-characters-to-glyphs"></a>Indo de caracteres para glifos

Agora que você sabe que a execução contém glifos verticais, você precisa obter acesso a esses glifos. No exemplo até agora, há 3 execuções: uma com glifos verticais e duas sem. Para fazer a transição de caracteres para glifos, você chama [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Esse método retorna os índices de glifos correspondentes para os caracteres no exemplo. Como o método [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) retorna uma execução com glifos verticais, você precisa chamar [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), que retorna as IDs de glifos verticalmente orientadas no lugar das IDs de glifo atuais.

## <a name="drawing-text-vertically"></a>Desenhar texto verticalmente

Por fim, você precisa dispor e desenhar o texto. Como você está desenhando o texto verticalmente, precisa obter mais informações para que o texto latino seja desenhado corretamente. Se você desenhar todo o texto ao longo da linha de base central, o texto latino aparecerá flutuando no meio da linha. Você precisa ter acesso à linha de base central e romano para alinhar o texto corretamente. Use o método [**IDWriteTextAnalyzer1:: Getbaseize**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) para obter os valores numéricos das linhas de base que você especificar. Você pode subtrair a linha de base Roman da linha de base central para obter o deslocamento entre os dois.

Com todas essas informações, você pode desenhar o texto na tela. Primeiro, chame o método [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) com os resultados dos objetos [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) .

Se você estiver usando o [Direct2D](rendering-by-using-direct2d.md) , também precisará definir a transformação mundial no destino de renderização Direct2D para a renderização vertical.

Por fim, chame [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) três vezes, uma vez em cada bloco de texto. Nos dois blocos de texto que estão em inglês, você precisa aplicar o deslocamento que calculamos entre as linhas de base Roman e central.

Agora, o texto em seu aplicativo será desenhado verticalmente, com a orientação de glifo correta.

 

 