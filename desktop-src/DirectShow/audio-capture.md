---
description: Captura de áudio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f76924e170c29e4488e2b7bd31bddbe8702ebe78d9ed146471bdfa21598d12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108706"
---
# <a name="audio-capture"></a>Captura de áudio

Um aplicativo pode usar DirectShow para capturar dados de áudio de microfones, players de fita e outros dispositivos, por meio das entradas na placa de som. Os cenários comuns são:

-   Gravação de uma narração de voiceover para posteriormente em um fluxo de vídeo.
-   Convertendo conteúdo de áudio análogo herdado em formato digital.
-   Captura de voz ou música para transmissão em uma rede.

Os usuários finais têm várias opções para capturar áudio da placa de som para o disco rígido. A maioria dos cartões fornece aplicativos para combinação e gravação de suas entradas de áudio. Windows fornece o Gravador de Som, um aplicativo utilitário simples para gravação de um microfone. O Windows media encoder pode ser incorporado em um aplicativo DirectShow como um objeto de mídia [directX](directx-media-objects.md) (DMO). Esta seção descreve como integrar a funcionalidade de captura de áudio em seu próprio aplicativo usando DirectShow.

Esta seção contém os seguintes tópicos:

-   [Sobre o filtro de captura de áudio](about-the-audio-capture-filter.md)
-   [Selecionando um dispositivo de captura](selecting-a-capture-device.md)
-   [Criando um sistema de captura de Graph](creating-an-audio-capture-graph.md)
-   [Criando um arquivo de captura de Graph com visualização](creating-an-audio-capture-graph-with-preview.md)
-   [Definindo propriedades de captura de áudio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow](using-directshow.md)
</dt> </dl>

 

 



