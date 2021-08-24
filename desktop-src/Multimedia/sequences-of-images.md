---
title: Sequências de imagens
description: Sequências de imagens
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, sequências de imagem
- DrawDib, sequência de bitmaps
- Função DrawDibDraw
- Função DrawDibBegin
- Função DrawDibEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac063cb2e9697b3b95045b95c9cc759a562197b56f10ff86a076ddcfa9a72cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688786"
---
# <a name="sequences-of-images"></a>Sequências de imagens

Você pode exibir uma sequência de bitmaps com as mesmas dimensões e formatos usando a [**função DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) com a [**função DrawDibBegin.**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) **DrawDibBegin** melhora a eficiência de **DrawDibDraw** preparando o DC DrawDib para desenho.

> [!Note]  
> Se o aplicativo não usar [**DrawDibBegin,**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) o executará implicitamente antes do desenho. Se seu aplicativo usa **DrawDibBegin** antes de **DrawDibDraw,** **DrawDibDraw** não precisa processar a função e aguardar a conclusão.

 

A [**função DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) fornece [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) com o DC DrawDib, o handle dc, o endereço da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e as dimensões de retângulo de origem e destino. Quando você exibe uma sequência de bitmaps, **DrawDibDraw** verifica os valores desses itens para cada imagem na sequência. Se **DrawDibDraw** detectar alterações em qualquer um desses itens, ele chamará implicitamente **DrawDibBegin** novamente para ajustar as configurações do DrawDib DC.

Depois de [**usar DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), você pode desenhar a sequência de imagem usando [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) e especificando um ou mais sinalizadores conforme apropriado. Especifique **o \_ sinalizador DDF SAME \_ HDC,** desde que o alça dc não tenha sido alterado. Especifique o sinalizador DDF SAME DRAW quando os seguintes parâmetros para DrawDibDraw não foram alterados: o endereço da estrutura \_ \_ [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)  e as dimensões do retângulo de origem e destino.

Você pode atualizar os sinalizadores definidos com [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) usando a [**função DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) seguida por outra chamada para **DrawDibBegin.** Em seguida, **use DrawDibEnd** para limpar o DC DrawDib de seus sinalizadores e configurações atuais. A chamada subsequente para **DrawDibBegin** reinicializa o DC DrawDib com os sinalizadores e as configurações apropriados. Como alternativa, você pode atualizar os sinalizadores para um DC DrawDib usando **DrawDibBegin** sem **DrawDibEnd.** Para fazer isso, você deve alterar pelo menos uma das seguintes configurações simultaneamente com os sinalizadores: o endereço da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) ou as dimensões do retângulo de origem ou destino.

Você pode aumentar a eficiência de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para operações de streaming de dados que usam imagens compactadas, como a reprodução de um clipe de vídeo, usando as funções [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) e [**DrawDibStop.**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) A **função DrawDibStart** prepara o DC DrawDib para receber um fluxo de imagens enviando uma mensagem para o VCM (gerenciador de compactação de vídeo). Quando o streaming terminar, **DrawDibStop** enviará uma mensagem ao VCM indicando que ele pode liberar recursos alocados para a operação de streaming de dados. Para obter mais informações sobre o VCM, consulte [Gerenciador de Compactação de Vídeo](video-compression-manager.md).

> [!Note]  
> Você deve especificar a largura e a altura dos retângulos de origem e destino em seu aplicativo. No entanto, você não precisa especificar as origens dos retângulos. Seu aplicativo pode redefinir as origens em [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para usar partes diferentes da imagem ou atualizar diferentes partes da exibição.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de imagem](image-rendering.md)
</dt> </dl>

 

 