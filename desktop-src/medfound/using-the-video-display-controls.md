---
description: Usando os controles de exibição de vídeo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Usando os controles de exibição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647731"
---
# <a name="using-the-video-display-controls"></a>Usando os controles de exibição de vídeo

A interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controla como o processador de vídeo avançado (EVR) exibe vídeo dentro de uma janela de aplicativo. Essa interface pode ser usada tanto no DirectShow quanto no Media Foundation. Internamente, os controles de exibição de vídeo são fornecidos pelo apresentador padrão da EVR. Se você escrever um apresentador personalizado, poderá fornecer a mesma interface ou definir uma interface personalizada.

A maneira correta de obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) depende se você está usando a versão do DIRECTSHOW do EVR ou a versão Media Foundation. Para o Media Foundation EVR, também depende se você está usando o EVR diretamente ou usando-o por meio da sessão de mídia (que é mais comum).

Para obter um ponteiro para a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , faça o seguinte:

1.  Obtenha um ponteiro para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .

    -   Se você estiver usando o filtro EVR do DirectShow, chame **QueryInterface** no filtro.

    -   Se você estiver usando o coletor de mídia do EVR diretamente, chame **QueryInterface** no coletor de mídia.

    -   Se você estiver usando a sessão de mídia, chame **QueryInterface** na sessão de mídia.

2.  Se você estiver usando a sessão de mídia, aguarde até que a sessão de mídia envie o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com um valor de status de MF \_ TOPOSTATUS \_ Ready. (Ignore esta etapa de outra forma.)

3.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . O identificador de serviço é o \_ serviço de renderização de vídeo Mr \_ \_ .

Você pode usar a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para executar as seguintes tarefas:

-   Defina a janela de recorte.

-   Defina os retângulos de origem e de destino.

-   Atualize a janela de vídeo em resposta a mensagens de janela.

-   Habilitar ou desabilitar o modo de tela inteira.

## <a name="clipping-window"></a>Janela de recorte

O aplicativo deve fornecer uma janela onde o EVR desenha o vídeo. Para definir a janela de recorte, chame [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) com um identificador para a janela do aplicativo.

Se você criar o coletor de mídia do EVR por meio de seu objeto de ativação, essa etapa não será necessária. O objeto de ativação chama automaticamente [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), usando o identificador de janela que você forneceu na função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .

## <a name="source-and-destination-rectangles"></a>Retângulos de origem e de destino

Durante a reprodução, o apresentador usa uma parte da imagem de vídeo compostada e a desenha em uma área da janela de vídeo. A parte da imagem composta é o retângulo de *origem* e a área da janela de vídeo é o retângulo de *destino*.

O retângulo de origem é definido usando coordenadas normalizadas em que o ponto (0,0, 0,0) corresponde ao canto superior esquerdo do vídeo e (1,0, 1,0) corresponde ao canto inferior direito do vídeo. O retângulo de origem pode ser qualquer região dentro deste retângulo. O retângulo de destino é especificado em pixels, em relação à área do cliente da janela. O retângulo de origem padrão é a imagem inteira e o retângulo de destino padrão é um retângulo vazio.

Para definir os retângulos de origem e de destino, chame [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Se você criar o coletor de mídia do EVR por meio de seu objeto de ativação, essa etapa não será necessária. O objeto de ativação define automaticamente o retângulo de destino igual a toda a área do cliente da janela. No entanto, você deve chamar [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) se quiser alterar o retângulo de origem ou definir um retângulo de destino diferente.

## <a name="window-messages"></a>Mensagens de janela

Durante a reprodução, o aplicativo deve responder a determinadas mensagens da janela, da seguinte maneira:

-   WM \_ Paint: chame [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) para redesenhar o vídeo. Além disso, evite pintar o retângulo de destino enquanto o vídeo está sendo reproduzido, pois isso pode causar oscilação.

-   \_Tamanho do WM: Talvez seja necessário chamar [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) para redimensionar o retângulo de destino.

Diferentemente do filtro de processador de mixagem de vídeo (VMR) no DirectShow, você não precisa notificar o EVR ao receber uma mensagem do WM \_ DISPLAYCHANGE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



