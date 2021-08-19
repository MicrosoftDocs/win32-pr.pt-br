---
description: Sobre o Vídeo Digital DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Sobre o Vídeo Digital DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664800"
---
# <a name="about-digital-video-in-directshow"></a>Sobre o Vídeo Digital DirectShow

O DV (vídeo digital) pode ser capturado de uma câmera DV, armazenado em um arquivo no computador do usuário ou armazenado em fita usando um VTR (gravador de fita de vídeo). Assim, as operações que um aplicativo pode executar em um fluxo DV incluem:

-   Capturar vídeo ao vivo de uma câmera DV.
-   Transmita dados DV da fita VTR para o computador.
-   Transmita dados DV do computador para o VTR.
-   Ler dados DV de um arquivo.
-   Gravar dados DV em um arquivo.
-   Renderizar o áudio e o vídeo em um fluxo DV.

DirectShow fornece os seguintes filtros DV:

-   [Driver MSDV](msdv-driver.md). O driver MSDV controla um dispositivo DV, como uma câmera. O dispositivo pode ter uma subunidade de câmera e uma subunidade VTR; O MSDV controla ambas as subunidades. O driver MSDV aparece para aplicativos como um DirectShow filtro.
-   [Filtro divisor DV.](dv-splitter-filter.md) Quadros DV contêm áudio e vídeo no mesmo quadro. O filtro divisor DV extrai os dados de áudio e os transmite como um ou dois fluxos de áudio. Ele transmite os dados originais como um fluxo de vídeo DV separado.
-   [Filtro de decodificador de vídeo DV.](dv-video-decoder-filter.md) Decodifica o vídeo DV em vídeo descompactado.
-   [Filtro codificador de vídeo DV.](dv-video-encoder-filter.md) Codifica vídeo descompactado em vídeo codificado em DV.
-   [DV Muxer](dv-muxer-filter.md). Combina um fluxo de vídeo DV com um ou dois fluxos de áudio para criar um único fluxo DV intercalado.

O Divisor de DV e o Decodificador de Vídeo DV funcionam juntos. O divisor leva o fluxo intercalado e saídas de áudio e fluxos de vídeo DV separados. O decodificador converte o vídeo DV em vídeo descompactado. A imagem a seguir ilustra esse processo.

![dv splitter e dv decoder](images/dv-filters1.png)

O Codificador de Vídeo DV e o DV Muxer invertem o processo: o codificador converte vídeo descompactado em vídeo DV e o mux combina áudio e vídeo DV para criar um único fluxo intercalado, conforme mostrado no diagrama a seguir.

![dv encoder e dv muxer](images/dv-filters2.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



