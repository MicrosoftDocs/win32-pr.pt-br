---
title: Pré-carregar patches com sintetizadores MIDI internos
description: Pré-carregar patches com sintetizadores MIDI internos
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- MIDI (Instrument Digital Interface Instrument), sintetizadores internos
- MIDI (Interface Digital Do instrumentar), sintetizadores internos
- reprodução de arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (Interface Digital do Instrument Instrument), pré-carregamento de patches
- MIDI (Interface Digital do Instrument Instrument), pré-carregamento de patches
- reprodução de arquivos MIDI, pré-carregamento de patches
- pré-carregamento de patches MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372493"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Pré-carregar patches com sintetizadores MIDI internos

Alguns dispositivos de sintetizador MIDI internos não podem manter todos os patches carregados simultaneamente. Esses dispositivos devem pré-carregar seus dados de patch.

Windows fornece as funções a seguir para solicitar que um pré-carregamento do sintetizador e os patches especificados sejam armazenados em cache.



| Valor                                                      | Significado                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Solicita que um dispositivo de sintetizador MIDI interno pré-carregar e armazenar em cache patches melodic especificados.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Solicita que um dispositivo de sintetizador MIDI interno pré-carregamento e cache de patches de patch baseados em chave especificados. |



 

Para obter informações sobre como determinar se um dispositivo específico dá suporte a patches de pré-carregamento, consulte [Consultando dispositivos de saída MIDI](querying-midi-output-devices.md).

 

 