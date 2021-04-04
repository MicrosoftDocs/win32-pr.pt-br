---
title: O mapeador de MIDI e o Windows
description: O mapeador de MIDI e o Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007481"
---
# <a name="the-midi-mapper-and-windows"></a>O mapeador de MIDI e o Windows

O mapeador de MIDI faz parte do software do sistema. A ilustração a seguir mostra como o mapeador de MIDI está relacionado a outros elementos dos serviços de áudio.

![como o mapeador de Midi está relacionado a outros elementos da imagem dos serviços de áudio](images/mmap-a01.gif)

Do ponto de vista de um aplicativo, o mapeador de MIDI parece outro dispositivo de saída MIDI. O mapeador de MIDI recebe mensagens enviadas a ele pelas funções de saída de MIDI de baixo nível [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) e [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg). O mapeador de MIDI modifica essas mensagens e as redireciona para um dispositivo de saída de MIDI de acordo com o mapa de configuração de MIDI atual. O mapa de instalação do MIDI atual é selecionado pelo usuário por meio da opção do painel de controle de MIDI. Somente o usuário pode selecionar o mapa de instalação atual; os aplicativos não podem alterar o mapa de instalação atual.

 

 