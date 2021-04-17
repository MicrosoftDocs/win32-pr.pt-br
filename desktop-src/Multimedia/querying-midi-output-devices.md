---
title: Consultando dispositivos de saída de MIDI
description: Consultando dispositivos de saída de MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de saída
- MIDI (interface digital de instrumentos musicais), dispositivos de saída
- executando arquivos MIDI, dispositivos de saída
- Dispositivos de saída MIDI
- MIDI (interface digital de instrumento musical), consultando dispositivos de saída
- MIDI (interface digital de instrumentos musicais), consultando dispositivos de saída
- executando arquivos MIDI, consultando dispositivos de saída
- consultando dispositivos de saída de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105775686"
---
# <a name="querying-midi-output-devices"></a>Consultando dispositivos de saída de MIDI

Antes de executar um arquivo MIDI, você deve usar a função [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) para determinar os recursos do dispositivo de saída MIDI que está presente no sistema. Essa função usa um endereço de uma estrutura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) , que preenche as informações sobre os recursos do determinado dispositivo. Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo (especificado nos membros **wMid**, **wPid**, **szPname** e **vDriverVersion** , respectivamente).

Os dispositivos de saída de MIDI podem ser sintetizadores internos ou portas de saída MIDI externas. O membro **wTechnology** da estrutura **MIDIOUTCAPS** especifica a tecnologia do dispositivo.

Se o dispositivo for um sintetizador interno, informações adicionais do dispositivo estarão disponíveis nos membros **wVoices**, **wNotes** e **wChannelMask** . O membro **wVoices** especifica o número de vozes às quais o dispositivo dá suporte. Cada voz pode ter um som ou timbre diferente. As vozes são organizadas em canais MIDI. O membro **wNotes** especifica o *Polyphony* do dispositivo — ou seja, o número máximo de notas que podem ser reproduzidas simultaneamente. O membro **wChannelMask** é uma representação de bit dos canais de MIDI para os quais o dispositivo responde. Por exemplo, se o dispositivo responder aos oito primeiros canais MIDI, **wChannelMask** será 0x00FF. Se o dispositivo for uma porta de saída externa, **wVoices** e **wNotes** não serão usados e **wChannelMask** será definido como 0xFFFF.

O membro **dwSupport** da estrutura **MIDIOUTCAPS** indica se o driver de dispositivo dá suporte a alterações de volume, cache de patch e streaming. As alterações de volume têm suporte apenas por dispositivos do sintetizador interno. As portas de saída MIDI externas não dão suporte a alterações de volume. Para obter informações sobre como alterar o volume, consulte [alterando o volume do sintetizador MIDI interno](changing-internal-midi-synthesizer-volume.md).

 

 