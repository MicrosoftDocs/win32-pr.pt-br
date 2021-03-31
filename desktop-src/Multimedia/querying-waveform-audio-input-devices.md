---
title: Consultando Waveform-Audio dispositivos de entrada
description: Consultando Waveform-Audio dispositivos de entrada
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- áudio de formato de onda, consultando dispositivos de entrada
- Wave-interface de áudio, consultando dispositivos de entrada
- gravando áudio de onda, consultando dispositivos de entrada
- consultando dispositivos de entrada de formato wave-áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917242"
---
# <a name="querying-waveform-audio-input-devices"></a>Consultando Waveform-Audio dispositivos de entrada

Antes de gravar áudio de onda, você deve chamar a função [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar os recursos de entrada de onda de áudio do sistema. Essa função preenche uma estrutura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) com informações sobre os recursos de um dispositivo especificado. Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo. Além disso, a estrutura **WAVEINCAPS** fornece informações sobre os formatos de áudio de forma de onda padrão aos quais o dispositivo dá suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 