---
description: Captura de áudio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296052"
---
# <a name="audio-capture"></a>Captura de áudio

Um aplicativo pode usar o DirectShow para capturar dados de áudio de microfones, players de fita e outros dispositivos, por meio das entradas na placa de som. Os cenários típicos incluem:

-   Gravando uma narração de VoiceOver para Dubbing posteriores em um fluxo de vídeo.
-   Convertendo conteúdo de áudio analógico herdado em formato digital.
-   Capturando voz ou música para transmissão em uma rede.

Os usuários finais têm várias opções para capturar áudio da placa de som para o disco rígido. A maioria dos cartões fornece aplicativos para misturar e gravar de suas entradas de áudio. O Windows fornece o gravador de som, um aplicativo utilitário simples para gravação de um microfone. O codificador do Windows Media pode ser incorporado em um aplicativo do DirectShow como um DMO ( [objeto de mídia do DirectX](directx-media-objects.md) ). Esta seção descreve como integrar a funcionalidade de captura de áudio em seu próprio aplicativo usando o DirectShow.

Esta seção contém os seguintes tópicos:

-   [Sobre o filtro de captura de áudio](about-the-audio-capture-filter.md)
-   [Selecionando um dispositivo de captura](selecting-a-capture-device.md)
-   [Criando um grafo de captura de áudio](creating-an-audio-capture-graph.md)
-   [Criando um grafo de captura de áudio com visualização](creating-an-audio-capture-graph-with-preview.md)
-   [Definindo propriedades de captura de áudio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 



