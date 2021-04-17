---
description: Pins de porta de vídeo na captura de arquivo
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Pins de porta de vídeo na captura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775590"
---
# <a name="video-port-pins-in-file-capture"></a>Pins de porta de vídeo na captura de arquivo

Se o dispositivo de captura tiver uma porta de vídeo, o PIN da porta de vídeo deverá ser conectado a um processador de vídeo, mesmo que você queira apenas capturar para um arquivo.

Se você chamar [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com o valor **fixar \_ categoria \_ Capture** e o dispositivo tiver um pino de porta de vídeo, o construtor do grafo de captura conectará automaticamente o PIN da porta de vídeo ao filtro do [mixer de sobreposição](overlay-mixer-filter.md) e conectará o mixer de sobreposição ao processador de vídeo. O construtor do grafo de captura oculta a janela de vídeo chamando [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) com o valor **OAFALSE**. Se o aplicativo mais tarde chamar **RenderStream** com a **\_ \_ visualização de categoria de PIN**, as chamadas do construtor de grafo de captura **colocarão \_ AutoShow** com o valor **OATRUE** para mostrar a janela de vídeo.

Depois de chamar **RenderStream** com **a \_ \_ captura de categoria de PIN**, você pode verificar se ele adicionou o processador de vídeo consultando o Gerenciador de gráfico de filtro para a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



