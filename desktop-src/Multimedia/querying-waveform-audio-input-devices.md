---
title: Consultando dispositivos Waveform-Audio entrada
description: Consultando dispositivos Waveform-Audio entrada
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- áudio waveform, consultando dispositivos de entrada
- interface waveform-audio, consultando dispositivos de entrada
- gravação de áudio de forma de onda, consultando dispositivos de entrada
- consultando dispositivos de entrada de áudio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371918"
---
# <a name="querying-waveform-audio-input-devices"></a>Consultando dispositivos Waveform-Audio entrada

Antes de gravar o áudio de forma de onda, você deve chamar a função [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar os recursos de entrada waveform-audio do sistema. Essa função preenche uma estrutura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) com informações sobre os recursos de um dispositivo especificado. Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo. Além disso, a **estrutura WAVEINCAPS** fornece informações sobre os formatos padrão waveform-audio compatíveis com o dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio waveform](recording-waveform-audio.md)
</dt> </dl>

 

 