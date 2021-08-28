---
title: Implementando IMediaObject AllocateStreamingResources
description: Implementando IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player plug-ins, recursos de streaming de exemplo de eco
- plug-ins, recursos de streaming de exemplo de eco
- plug-ins de processamento de sinal digital, recursos de streaming de exemplo de eco
- Plug-ins do DSP, recursos de streaming de exemplo de eco
- Exemplo de plug-in do DSP de eco, recursos de streaming
- Exemplo de plug-in do DSP de eco, buffer de atraso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291b1f9627d9dfb78ae2aff9d34b6fadd47cbf28a5c2f0830f5833d9e83cde21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508956"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementando IMediaObject::AllocateStreamingResources

No exemplo echo, o **método AllocateStreamingResources** cria o buffer de atraso. Ele faz isso fazendo o seguinte:

1.  Calculando um tamanho para o buffer que corresponde ao tempo de atraso especificado para o tipo de mídia especificado.
2.  Alocar nova memória ou realocar o tamanho do buffer, se ele já existir.
3.  Chamar um método que preenche o buffer com valores que representam silêncio.

O valor de silêncio é diferente dependendo da profundidade do bit. Para áudio de 8 bits, o silêncio é representado pelo valor hexatorial 80; para áudio de 16 bits, o silêncio é representado por zero.

## <a name="calculating-the-delay-buffer-size"></a>Calculando o tamanho do buffer de atraso

Para calcular o tamanho necessário para o buffer de atraso, você deve primeiro recuperar uma estrutura **WAVEFORMATEX** que contém informações sobre os dados de áudio. O exemplo a seguir recupera um ponteiro para essa estrutura da estrutura de entrada **DMO \_ MEDIA \_ TYPE:**


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Depois de armazenar um ponteiro para a estrutura **WAVEFORMATEX** adequada, você pode inspecionar seus membros e usá-los para calcular o tamanho do buffer necessário. O exemplo de código a seguir demonstra isso:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Esse algoritmo calcula o tamanho do buffer multiplicando o tempo de atraso, em milissegundos, pelo número de amostras por milissegundos, multiplicando o resultado pelo número de canais e multiplicando o resultado pelo número de bytes por amostra. O número de canais e o número de bytes por amostra não são óbvios; eles são codificados no membro nBlockAlign. Dividir por 1000 reduz o valor nSamplesPerSec para amostras por milissegundos; o milissegundo é a unidade desejada porque o tempo de atraso é expresso em milissegundos.

## <a name="allocating-the-delay-buffer-memory"></a>Alocando a memória do buffer de atraso

Depois de calcular os requisitos de memória, você pode alocar o buffer. O buffer pode precisar ser excluído se ele existir, como quando o usuário invoca a página de propriedades para alterar o valor do tempo de atraso. O código a seguir demonstra a alocação do buffer de atraso:


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



Se o buffer for alocado com êxito, você deverá mover o ponteiro móvel para o cabeça do buffer, conforme demonstrado no exemplo a seguir:


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



Lembre-se de adicionar a declaração de encaminhamento para a função ao arquivo de header Echo.h na seção privada:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Você deve adicionar código no final de AllocateStreamingResources para chamar esse método sempre que o buffer de atraso for criado ou ressalto. O código de exemplo a seguir passa o ponteiro WAVEFORMATEX chamado pWave para o novo método:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Realocando a memória do buffer de atraso

Quando o usuário altera o tempo de atraso usando a página de propriedades, o tamanho do buffer de atraso também deve mudar. Você já adicionou o código a AllocateStreamingResources para reorganizar o buffer, mas precisa adicionar uma linha de código ao atraso de CEcho::p ut para chamar o método de alocação de recursos sempre que o valor da propriedade \_ mudar. Eis o código:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




