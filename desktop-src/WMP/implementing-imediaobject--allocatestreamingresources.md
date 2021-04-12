---
title: Implementando IMediaObject AllocateStreamingResources
description: Implementando IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Plug-ins do Windows Media Player, recursos de streaming de amostra de eco
- plug-ins, amostras de eco de recursos de streaming
- plug-ins de processamento de sinal digital, Echo amostras de recursos de streaming
- Plug-ins do DSP, amostras de eco de recursos de streaming
- Exemplo de plug-in de eco do DSP, recursos de streaming
- Exemplo de plug-in do eco DSP, buffer de atraso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364129"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementando IMediaObject:: AllocateStreamingResources

No exemplo de eco, o método **AllocateStreamingResources** cria o buffer de atraso. Ele faz isso fazendo o seguinte:

1.  Calculando um tamanho para o buffer que corresponde ao tempo de atraso especificado para o tipo de mídia fornecido.
2.  Alocar uma nova memória ou realocar o tamanho do buffer se ele já existir.
3.  Chamar um método que preenche o buffer com valores que representam silêncio.

O valor de silêncio é diferente, dependendo da profundidade de bits. Para áudio de 8 bits, o silêncio é representado pelo valor hexadecimal 80; para áudio de 16 bits, o silêncio é representado por zero.

## <a name="calculating-the-delay-buffer-size"></a>Calculando o tamanho do buffer de atraso

Para calcular o tamanho necessário para o buffer de atraso, você deve primeiro recuperar uma estrutura **WAVEFORMATEX** que contém informações sobre os dados de áudio. O exemplo a seguir recupera um ponteiro para essa estrutura da estrutura **de \_ \_ tipo de mídia DMO** de entrada:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Depois de armazenar um ponteiro para a estrutura **WAVEFORMATEX** apropriada, você pode inspecionar seus membros e usá-los para calcular o tamanho do buffer necessário. O exemplo de código a seguir demonstra isso:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Esse algoritmo computa o tamanho do buffer multiplicando o tempo de atraso, em milissegundos, pelo número de amostras por milissegundo, multiplicando o resultado pelo número de canais e, em seguida, multiplicando o resultado pelo número de bytes por amostra. O número de canais e o número de bytes por amostra não são óbvios; Eles são codificados no membro nBlockAlign. Dividir por 1000 reduz o valor de nSamplesPerSec para amostras por milissegundo; o milissegundo é a unidade desejada porque o tempo de atraso é expresso em milissegundos.

## <a name="allocating-the-delay-buffer-memory"></a>Alocando a memória de buffer de atraso

Depois de calcular os requisitos de memória, você pode alocar o buffer. O buffer pode precisar ser excluído se existir, por exemplo, quando o usuário chamar a página de propriedades para alterar o valor do tempo de atraso. O código a seguir demonstra a alocação do buffer de atraso:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



Se o buffer for alocado com êxito, você deverá mover o ponteiro móvel para o cabeçalho do buffer, conforme demonstrado no exemplo a seguir:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Preenchendo o buffer de atraso com silêncio

É conveniente escrever um método para preencher o buffer de atraso com valores que representam silêncio. O método deve receber o ponteiro para a estrutura WAVEFORMATEX válida e, em seguida, inspecionar o membro wBitsPerSample para determinar se o áudio é de 8 bits ou superior. O exemplo a seguir preenche o buffer de atraso com o valor correto para silêncio:


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



Lembre-se de adicionar a declaração de encaminhamento da função ao arquivo de cabeçalho Echo. h na seção particular:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Você deve adicionar o código ao final de AllocateStreamingResources para chamar esse método sempre que o buffer de atraso for criado ou redimensionado. O código de exemplo a seguir passa o ponteiro WAVEFORMATEX chamado pWave para o novo método:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Realocando a memória de buffer de atraso

Quando o usuário altera o tempo de atraso usando a página de propriedades, o tamanho do buffer de atraso também deve ser alterado. Você já adicionou o código a AllocateStreamingResources para redimensionar o buffer, mas precisa adicionar uma linha de código ao CEcho::p o \_ atraso de UT para chamar o método de alocação de recursos sempre que o valor da propriedade for alterado. Eis o código:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




