---
title: A arquitetura do mapeador de MIDI
description: A arquitetura do mapeador de MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, arquitetura
- Mapeador de MIDI, mapa de instalação
- Mapa de instalação MIDI
- Mapeador de MIDI, mapa de canal
- Mapeador de MIDI, mapas de patch
- Mapeador de MIDI, mapas de chave
- mapa de canal
- mapas de patch
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a20e73c9a361487468870698d3c36d59ef35bb6a28da1b03957dd24f1d7b7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136394"
---
# <a name="the-midi-mapper-architecture"></a>A arquitetura do mapeador de MIDI

O mapeador de MIDI usa um mapa de instalação de MIDI para determinar como converter e redirecionar as mensagens recebidas. Um mapa de instalação de MIDI consiste nos seguintes tipos de mapas.

-   [O mapa do canal](the-channel-map.md)
-   [Mapas de patch](patch-maps.md)
-   [Mapas de chave](key-maps.md)

A ilustração a seguir mostra as funções de canal, patch e mapas de chave em um mapa de instalação de MIDI.

![as funções de canal, patch e mapas de chave em uma imagem de mapa de instalação Midi](images/mmap-a02.gif)

 

 




