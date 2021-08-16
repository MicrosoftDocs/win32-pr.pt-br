---
title: Processando os dados de áudio
description: Processando os dados de áudio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- plug-ins de Windows Media Player, método Echo de exemplo DoProcessOutput
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, dados de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678e1debd586017bfbe748d4f2bed6d17607afcbe2719b5e3ecba8cabf667af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334479"
---
# <a name="processing-the-audio-data"></a>Processando os dados de áudio

A implementação padrão de **DoProcessOutput** começa pela recuperação de um ponteiro para uma estrutura **WAVEFORMATEX** válida, exatamente como foi feita em **AllocateStreamingResources**. Em seguida, ele usa as informações nessa estrutura para calcular o número de amostras no buffer de entrada aguardando processamento. O código a seguir é da implementação padrão:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Em seguida, o código inspeciona o membro **wBitsPerSample** para determinar a profundidade de bits do áudio. Esse valor é usado em uma instrução switch para fornecer processamento separado para áudio de 8 e 16 bits.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Diferenças entre áudio de 8 e 16 bits

Há diferenças importantes entre áudio de 8 e 16 bits. Portanto, as rotinas de processamento para criar o efeito de eco são diferentes. Os dois formatos diferem das seguintes maneiras:

-   Cada formato tem um tamanho de amostra diferente: amostras de 8 bits cada ocupam um byte de memória, enquanto os exemplos de 16 bits ocupam dois bytes.
-   Cada formato representa a amplitude de áudio de forma diferente. o áudio de 8 bits é representado por um inteiro sem sinal com um intervalo de 0 a 255; um valor de 128 representa silêncio. áudio de 16 bits é representado por um inteiro assinado com um intervalo de-32768 a 32767; um valor de zero representa silêncio.

Embora o processo de criação do efeito de eco seja fundamentalmente idêntico para cada formato, os detalhes devem ser ligeiramente diferentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




