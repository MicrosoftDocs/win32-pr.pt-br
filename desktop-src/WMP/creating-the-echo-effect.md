---
title: Criando o efeito de eco
description: Criando o efeito de eco
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in de eco do DSP, criando efeito de eco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004956"
---
# <a name="creating-the-echo-effect"></a>Criando o efeito de eco

Primeiro, você deve remover o código do exemplo de assistente que dimensiona o áudio. Na seção de 8 bits, remova o seguinte código:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



(Lembre-se de que m \_ fScaleFactor foi substituído por m \_ dwDelayTime.)

Na seção de 16 bits, remova o seguinte código:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



A implementação de **DoProcessOutput** fornecida pelo código de exemplo do assistente de plug-in cria um loop while que itera uma vez para cada amostra no buffer de entrada fornecido pelo Windows Media Player. Esse loop funciona da mesma maneira para áudio de 8 e 16 bits, embora um loop separado seja necessário para cada um. Em cada caso, o loop é iniciado com o teste a seguir:


```C++
while (dwSamplesToProcess--)

```



Uma vez dentro do loop, as rotinas de processamento são muito semelhantes para áudio de 8 e 16 bits. A principal diferença é que o código na seção de 8 bits altera o intervalo de valores de dados para-128 até 127 e, em seguida, converte o intervalo novamente antes de gravar os dados no buffer de saída. Isso é importante para manter a simetria da onda de áudio durante o processamento.

Agora você pode começar a adicionar e substituir o código no loop de processamento.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Recuperar um exemplo do buffer de entrada

Durante cada iteração do loop, um único exemplo é recuperado do buffer de entrada. Para áudio de 8 bits, o exemplo é deslocado para o novo intervalo e, em seguida, o ponteiro para o buffer de entrada é avançado para o próximo exemplo. O código a seguir é do assistente de plug-in:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Para áudio de 16 bits, o processo é o mesmo, exceto para a normalização:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Lembre-se de que os ponteiros no código de 16 bits foram convertidos em tipo **curto**.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Recuperar um exemplo do buffer de atraso

Em seguida, recupere um único exemplo do buffer de atraso. Para o código de 8 bits, os exemplos de atraso são armazenados em seu intervalo nativo de 0 a 255. O código a seguir, que você deve adicionar, recupera um exemplo de atraso de 8 bits:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Para áudio de 16 bits, o processo é semelhante:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Gravar a amostra de entrada no buffer de atraso

Agora, você deve armazenar o exemplo de entrada no buffer de atraso no mesmo local do qual você recuperou o exemplo de atraso. Este é o código que você deve adicionar para áudio de 8 bits:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Este é o código a ser adicionado para a seção de 16 bits:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Mover o ponteiro de buffer de atraso

Agora que o trabalho no buffer de atrasos foi concluído para essa iteração, você pode avançar o ponteiro móvel para o buffer de atraso. Se o ponteiro atingir o final do buffer circular, você deverá alterar seu valor para apontar para o cabeçalho do buffer. Para fazer isso para áudio de 8 bits, use o seguinte código:


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Este é o código para a seção de 16 bits:


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Como o ponteiro na seção de 16 bits é realmente uma cópia da variável de membro, você deve se lembrar de atualizar o valor na variável de membro com o novo endereço. Se você não conseguir fazer isso, o ponteiro de buffer de atraso apontará para o cabeçalho do buffer repetidamente e o efeito de eco não funcionará conforme o esperado. Adicione o seguinte código à seção de 16 bits:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Misturar o exemplo de entrada com a amostra de atraso

É aqui que você usa os valores de mistura úmida e seca de misturas para criar o exemplo de saída final. Basta multiplicar cada amostra pelo valor de ponto flutuante que representa a porcentagem do sinal final para o exemplo. Multiplique a amostra de entrada pelo valor armazenado em m \_ fDryMix; multiplique a amostra de atraso pelo valor armazenado em m \_ fWetMix. Em seguida, adicione os dois valores. O código que você deve adicionar é idêntico para as seções de 8 e 16 bits:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Gravar os dados no buffer de saída

Por fim, copie o exemplo misto para o buffer de saída e, em seguida, avance o ponteiro de buffer de saída. Para áudio de 8 bits, o assistente de plug-in usa o seguinte código para retornar o exemplo ao seu intervalo original:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Para áudio de 16 bits, o assistente usa o seguinte código como a etapa final no loop de processamento:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




