---
title: Mapas de chave
description: Mapas de chave
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapas de chave
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72197de28a6596efa951b302f0ca351ac187532cd28d431cf1d954b53d841064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140215"
---
# <a name="key-maps"></a>Mapas de chave

Cada entrada na tabela de tradução do mapa de patches pode ter um mapa de chaves associado. Os mapas principais afetam as mensagens de observação, de observação e de aftertouch de chave de telefonia. Um mapa de chaves tem uma tabela de conversão com uma entrada para cada um dos valores de chave MIDI 128. Por exemplo, se a entrada para o valor de chave 60 for 72, o mapeador de MIDI modificará as mensagens de observação em MIDI, conforme mostrado na ilustração a seguir.

![imagem do Mapeador MIDI](images/mmap-a06.gif)

Mapas de chave são úteis com sintetizadores que têm instrumentos de percussão baseados em chave com um som de percussão específico atribuído a cada chave. Mapas de chave geralmente são atribuídos ao primeiro patch no mapa de patches nos canais de percussão (10 e 16).

 

 




