---
title: Implementando DoProcessOutput
description: Implementando DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, DoProcessOutput
- Plug-ins do DSP, DoProcessOutput
- plug-ins do DSP de áudio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364109"
---
# <a name="implementing-doprocessoutput"></a>Implementando DoProcessOutput

Para processar dados de áudio, você precisará executar várias etapas em **DoProcessOutput**. As etapas a seguir usam o código de exemplo do assistente de plug-in como exemplos. Se você quiser criar um plug-in de DSP de áudio que processa o conteúdo de mídia do mesmo tipo que o código de exemplo do assistente de plug-in, você só precisará alterar o código de processamento real mencionado na etapa 6. A seguir estão todas as etapas implementadas no **DoProcessOutput**:

-   Se o plug-in não estiver habilitado no momento, basta copiar os dados inalterados no buffer de saída. Se o seu plug-in converter os dados em um formato diferente, você também deverá fazer o processamento de conversão aqui.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Recupere um ponteiro para a estrutura de formato de entrada. Você precisará recuperar dados do membro dessa estrutura, portanto, copie o ponteiro de *m \_ mtInput*.**pbFormat** para uma variável de ponteiro local de um tipo que corresponde ao tipo de estrutura de formato. O exemplo a seguir armazena um ponteiro para uma estrutura de formato de entrada **WAVEFORMATEX** :

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Calcule o número de amostras a serem processadas. O código de exemplo gerado pelo assistente de plug-in executa essa etapa dividindo o número de bytes a serem processados pelo membro **nBlockAlign** da estrutura de formato de entrada WAVEFORMATEX e, em seguida, multiplicando o resultado pelo número de canais, que foi armazenado no membro **nChannels** . O exemplo a seguir é do código de exemplo do assistente de plug-in:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Determine a profundidade de bits do áudio. O código de exemplo do assistente de plug-in determina o áudio de 8 ou 16 bits inspecionando o membro **wBitsPerSample** da estrutura **WAVEFORMATEX** . Em seguida, ele usa esse valor em uma instrução switch para fornecer rotinas de processamento separadas para cada profundidade de bits. Talvez seja necessário usar uma técnica diferente ao lidar com outros tipos de formato e profundidades de bits.
    2.  Crie um loop para percorrer os exemplos de áudio no buffer de entrada.
    3.  Recupere um exemplo do buffer de entrada. Você faz isso desreferenciando o ponteiro de dados de entrada e armazenando o resultado em uma variável do tipo int. Para áudio de 16 bits, você deve reconverter o ponteiro de BYTE para um ponteiro curto para lidar com a precisão de amostra de áudio maior. Quando tiver o valor, você poderá incrementar imediatamente o ponteiro *pbInputData* para que ele aponte para o próximo exemplo. Os exemplos a seguir demonstram isso:

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    – ou –

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  Execute o processamento. É aqui que você aplica os algoritmos que alteram o exemplo de alguma forma. O que você faz aqui é para você.
    2.  Grave os dados processados no buffer de saída. Incrementar imediatamente o ponteiro para o buffer de saída, como no exemplo a seguir:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Repita o loop até que todos os exemplos tenham sido processados.
    2.  Retornar um **HRESULT** apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




