---
description: Pinos de porta de vídeo na Captura de Arquivos
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Pinos de porta de vídeo na Captura de Arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049376"
---
# <a name="video-port-pins-in-file-capture"></a>Pinos de porta de vídeo na Captura de Arquivos

Se o dispositivo de captura tiver uma porta de vídeo, o pino da porta de vídeo deverá estar conectado a um renderador de vídeo, mesmo que você queira apenas capturar um arquivo.

Se você chamar [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com o valor **PIN CATEGORY \_ \_ CAPTURE** e o dispositivo tiver um pin de porta de vídeo, o Construtor do Graph de Captura conectará automaticamente o pino da porta de vídeo ao filtro [sobreposição Mixer](overlay-mixer-filter.md) e conectará o Mixer de sobreposição ao Renderador de Vídeo. O Construtor Graph Captura oculta a janela de vídeo chamando [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) com o valor **OAFALSE**. Se o aplicativo chamar posteriormente **RenderStream** com **PIN CATEGORY \_ \_ PREVIEW,** as chamadas do Construtor de Graph de Captura colocarão **\_ AutoShow** com o valor **OATRUE** para mostrar a janela de vídeo.

Depois de chamar **RenderStream** com **PIN CATEGORY \_ \_ CAPTURE**, você poderá verificar se ele adicionou o Renderização de Vídeo consultando o Gerenciador de filtros Graph para a interface [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



