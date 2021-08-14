---
title: Precarregamento de patches com sintetizadores MIDI internos
description: Precarregamento de patches com sintetizadores MIDI internos
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- MIDI (interface digital de instrumento musical), sintetizadores internos
- MIDI (interface digital de instrumentos musicais), sintetizadores internos
- executando arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (interface digital de instrumento musical), patches de pré-carregamento
- MIDI (interface digital de instrumentos musicais), patches de pré-carregamento
- executando arquivos MIDI, caminhos de pré-carregamento
- carregando patches de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372493"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Precarregamento de patches com sintetizadores MIDI internos

Alguns dispositivos de sintetizador MIDI internos não podem manter todos os seus patches carregados simultaneamente. Esses dispositivos devem pré-carregar seus dados de patch.

Windows fornece as seguintes funções para solicitar que um sintetizador seja pré-carregar e armazene em cache os patches especificados.



| Valor                                                      | Significado                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Solicita que um dispositivo sintetizador MIDI interno seja pré-carregamento e armazene em cache os patches Melodic especificados.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Solicita que um dispositivo sintetizador MIDI interno seja despré-carregamento e armazene em cache os patches de percussão baseados em chave especificados. |



 

Para obter informações sobre como determinar se um dispositivo específico dá suporte a patches de pré-carregamento, consulte [consultando dispositivos de saída de Midi](querying-midi-output-devices.md).

 

 