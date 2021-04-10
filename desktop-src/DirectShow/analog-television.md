---
description: Televisão analógica
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisão analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087516"
---
# <a name="analog-television"></a>Televisão analógica

A televisão analógica difere de outros cenários de captura de vídeo de várias maneiras:

-   O cartão sintonizador ajusta-se a um sinal analógico, que é então digitalizado.
-   O áudio é transportado no sinal analógico. A maneira como o áudio atinge a placa de som varia dependendo do hardware.
-   O sinal pode conter dados adicionais no intervalo vertical em branco (VBI), como legendas codificadas (CC), teletexto mundial padrão (WST) e serviços de dados estendidos (XDS).

O diagrama a seguir mostra um grafo de filtro típico para visualização de televisão.

![gráfico de televisão analógica](images/vidcap06.png)

-   O filtro de [sintonizador de TV](tv-tuner-filter.md) controla o ajuste.
-   O filtro de [áudio de TV](tv-audio-filter.md) controla a decodificação de áudio.
-   Se o cartão sintonizador tiver mais de uma entrada física, o filtro [Crossbar de vídeo analógico](analog-video-crossbar-filter.md) permitirá que o aplicativo selecione qual entrada é decodificada e renderizada.
-   O filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) entrega o fluxo de vídeo digitalizado.

O construtor de grafo de captura insere automaticamente todos os filtros necessários para o upstream a partir do filtro de captura.

Esta seção contém os seguintes tópicos:

-   [Ajuste de televisão analógica](analog-television-tuning.md)
-   [Áudio de televisão analógica](analog-television-audio.md)
-   [Legendas e teletextos codificados](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



