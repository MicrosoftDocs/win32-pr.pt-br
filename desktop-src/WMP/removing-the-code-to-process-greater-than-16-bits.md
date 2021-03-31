---
title: Removendo o código para processar mais de 16 bits
description: Removendo o código para processar mais de 16 bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, processando mais de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822651"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>Removendo o código para processar mais de 16 bits

Como este exemplo só processa áudio de 8 ou 16 bits, você precisa modificar o código em **CEcho:: ValidateMediaType** para retornar o \_ tipo DMO E \_ \_ não \_ aceito para tipos de mídia maiores que 16 bits. Para fazer isso, você deve alterar o código no bloco switch que testa os formatos do tipo WAVE \_ Format \_ extensível. Substitua o código do assistente pelo seguinte código de exemplo:


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



Em seguida, exclua ou comente as seções de código em **DoProcessOutput** que lidam com áudio de alta resolução de bits. Essas são as seções que começam com o caso 24 e o caso 32.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




