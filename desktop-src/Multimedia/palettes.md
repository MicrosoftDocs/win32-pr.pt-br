---
title: Paletas
description: Paletas
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, paletas
- Função DrawDibRealize
- Função DrawDibDraw
- Função DrawDibSetPalette
- Função DrawDibGetPalette
- Função DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917260"
---
# <a name="palettes"></a>Paletas

As funções DrawDib exigem que um aplicativo responda a duas mensagens orientadas a paleta: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) e [**WM \_ paletachanged**](/windows/desktop/gdi/wm-palettechanged). Se seu aplicativo não reconhecer a paleta, você precisará adicionar um manipulador para cada uma dessas mensagens. Para obter mais informações sobre como processar as mensagens do **WM \_ QUERYNEWPALETTE** e do **WM da \_ Paletachanged** , consulte [adicionando manipuladores de mensagens da paleta](adding-palette-message-handlers.md).

Você pode obter a paleta DrawDib atual para o controlador de domínio usando a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) . Você deve perceber a paleta em resposta à mensagem do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) ou do [**WM da \_ paletachanged**](/windows/desktop/gdi/wm-palettechanged) ou ao se preparar para exibir uma sequência de imagens usando a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

Você pode desenhar uma imagem mapeada para outra paleta usando a função [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) . Essa função força o controlador de domínio DrawDib a usar a paleta especificada, o que pode afetar a qualidade da imagem. Por exemplo, um aplicativo com reconhecimento de paleta pode ter percebido uma paleta e precisa impedir que o DrawDib perceba sua própria paleta. O aplicativo pode usar **DrawDibSetPalette** para notificar o DrawDib da paleta a ser usada.

Você pode obter um identificador da paleta de primeiro plano atual usando a função [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) . Se seu aplicativo usar a paleta de primeiro plano atual, ele não terá o uso exclusivo da paleta e outro aplicativo poderá invalidar o identificador da paleta. Seu aplicativo não deve liberar a paleta quando você terminar de usá-la. A liberação da paleta pode invalidar o identificador da paleta para outro aplicativo.

Você pode preparar o DrawDib para receber novos valores de cor para sua paleta usando a função [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) . No código a seguir **DrawDibChangePalette**, você atribui novos valores para a tabela de cores da paleta. Se o sinalizador de **\_ animação do DDF** não estiver definido no controlador de domínio DrawDib quando você chamar **DrawDibChangePalette**, você poderá aplicar as alterações da paleta usando [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para perceber a paleta. Em seguida, você pode usar [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para redesenhar a imagem. Se o sinalizador de **\_ animação do DDF** for definido no DrawDib DC, você poderá animar a paleta e as cores do bitmap exibido usando **DrawDibDraw** ou **DrawDibRealize**. Você pode atualizar o sinalizador de **\_ animação do DDF** usando as funções [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) e [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) .

> [!Note]  
> Se você liberar a paleta DrawDib enquanto ela estiver selecionada por um controlador de domínio, um erro de GDI (interface de dispositivo gráfico) poderá resultar quando o DC usar a paleta. Em vez disso, seu aplicativo deve usar [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) para alterar o controlador de domínio DrawDib para usar a paleta padrão ou outra paleta.

 

As funções [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)e [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) podem liberar a paleta DrawDib. No entanto, essas funções devem ser usadas somente quando a paleta não tiver sido selecionada pelo controlador de domínio. A função DrawDibDraw também pode liberar a paleta quando ela usa o mesmo controlador de domínio DrawDib, mas especifica parâmetros de desenho diferentes (*lpbi*, *dxDst*, *dyDst*, *dxSrc* ou *dySrc*) ou um formato diferente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de imagem](image-rendering.md)
</dt> </dl>

 

 