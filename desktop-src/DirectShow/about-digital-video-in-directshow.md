---
description: Sobre vídeo digital no DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Sobre vídeo digital no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664800"
---
# <a name="about-digital-video-in-directshow"></a>Sobre vídeo digital no DirectShow

O vídeo digital (DV) pode ser capturado de uma câmera DV, armazenada em um arquivo no computador do usuário ou armazenada em fita usando um gravador de fita de vídeo (VTR). Portanto, as operações que um aplicativo pode executar em um fluxo de DV incluem:

-   Capture o vídeo ao vivo de uma câmera de vídeo digital.
-   Transmita dados DV da fita VTR para o computador.
-   Transmita dados DV do computador para o VTR.
-   Ler dados de DV de um arquivo.
-   Gravar dados DV em um arquivo.
-   Renderizar o áudio e o vídeo em um fluxo de DV.

DirectShow fornece os seguintes filtros de DV:

-   [Driver MSDV](msdv-driver.md). O driver MSDV controla um dispositivo DV, como uma camcorder. O dispositivo pode ter uma subunidade de câmera e uma subunidade VTR; MSDV controla ambas as subunidades. o driver MSDV aparece para aplicativos como um filtro DirectShow.
-   Filtro de [Splitter de DV](dv-splitter-filter.md) . Os quadros de DV contêm áudio e vídeo no mesmo quadro. O filtro de Splitter de DV extrai os dados de áudio e os gera como um ou dois fluxos de áudio. Ele gera os dados originais como um fluxo de vídeo DV separado.
-   Filtro de [decodificador de vídeo DV](dv-video-decoder-filter.md) . Decodifica vídeo DV em vídeo descompactado.
-   Filtro de [codificador de vídeo DV](dv-video-encoder-filter.md) . Codifica vídeo descompactado para vídeo codificado em DV.
-   [Muxer DV](dv-muxer-filter.md). Combina um fluxo de vídeo DV com um ou dois fluxos de áudio, para criar um fluxo de DV único intercalado.

O separador de vídeo DV e o decodificador DV Video funcionam juntos. O divisor usa o fluxo intercalado e gera fluxos de vídeo de áudio e DV separados. O decodificador converte o vídeo DV em vídeo descompactado. A imagem a seguir ilustra esse processo.

![divisor DV e codificador DV](images/dv-filters1.png)

O codificador de vídeo DV e o DV Muxer reverte o processo: o codificador converte vídeo descompactado em vídeo DV e o MUX combina áudio e vídeo DV para criar um fluxo intercalado único, conforme mostrado no diagrama a seguir.

![codificador DV e DV Muxer](images/dv-filters2.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



