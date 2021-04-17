---
title: Sequências de imagens
description: Sequências de imagens
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, sequências de imagens
- DrawDib, sequência de bitmaps
- Função DrawDibDraw
- Função DrawDibBegin
- Função DrawDibEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105811829"
---
# <a name="sequences-of-images"></a>Sequências de imagens

Você pode exibir uma sequência de bitmaps com as mesmas dimensões e formatos usando a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) com a função [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) . O **DrawDibBegin** melhora a eficiência do **DrawDibDraw** ao preparar o DC do DrawDib para desenho.

> [!Note]  
> Se seu aplicativo não usar [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) o executará implicitamente antes do desenho. Se seu aplicativo usar **DrawDibBegin** antes de **DrawDibDraw**, o **DrawDibDraw** não precisará processar a função e esperar que ela seja concluída.

 

A função [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) fornece [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) com o controlador de domínio DrawDib, o identificador de DC, o endereço da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e as dimensões de retângulo de origem e de destino. Quando você exibe uma sequência de bitmaps, o **DrawDibDraw** verifica os valores desses itens para cada imagem na sequência. Se **DrawDibDraw** detectar alterações em qualquer um desses itens, ele chamará implicitamente o **DrawDibBegin** novamente para ajustar as configurações de DC do DrawDib.

Depois de usar o [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), você pode desenhar a sequência de imagens usando [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) e especificando um ou mais sinalizadores conforme apropriado. Especifique o **\_ mesmo sinalizador \_ HDC do DDF** , contanto que o identificador do controlador de domínio não tenha sido alterado. Especifique o \_ mesmo sinalizador de desenho do DDF \_ quando os seguintes parâmetros para **DrawDibDraw** não forem alterados: o endereço da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) e as dimensões do retângulo de origem e de destino.

Você pode atualizar os sinalizadores definidos com [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) usando a função [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) seguida por outra chamada para **DrawDibBegin**. Em seguida, use **DrawDibEnd** para limpar o controlador de domínio DrawDib de seus sinalizadores e configurações atuais. A chamada subsequente para **DrawDibBegin** reinicializa o controlador de domínio DrawDib com os sinalizadores e as configurações apropriadas. Como alternativa, você pode atualizar os sinalizadores para um DrawDib DC usando **DrawDibBegin** sem **DrawDibEnd**. Para fazer isso, você deve alterar pelo menos uma das seguintes configurações simultaneamente com os sinalizadores: o endereço da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) ou as dimensões de retângulo de origem ou de destino.

Você pode aumentar a eficiência do [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para operações de streaming de dados que usam imagens compactadas, como reproduzir um clipe de vídeo, usando as funções [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) e [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) . A função **DrawDibStart** prepara o controlador de domínio DrawDib para receber um fluxo de imagens enviando uma mensagem para o Gerenciador de compactação de vídeo (VCM). Quando o streaming termina, o **DrawDibStop** envia uma mensagem para VCM indicando que ele pode liberar os recursos alocados para a operação de streaming de dados. Para obter mais informações sobre VCM, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md).

> [!Note]  
> Você deve especificar a largura e a altura dos retângulos de origem e de destino em seu aplicativo. No entanto, não é necessário especificar as origens dos retângulos. Seu aplicativo pode redefinir as origens em [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para usar diferentes partes da imagem ou para atualizar partes diferentes da exibição.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de imagem](image-rendering.md)
</dt> </dl>

 

 