---
description: Você pode alterar grafos de áudio a qualquer momento para adicionar ou remover vozes ou subgrafos inteiros.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090680"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio

Você pode alterar grafos de áudio a qualquer momento para adicionar ou remover vozes ou subgrafos inteiros. Este tópico mostra como adicionar ou remover vozes submix de um grafo criado seguindo as etapas em [como compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md). Uma única voz pode enviar sua saída para várias vozes ou para uma cadeia de vozes longa. Remover ou adicionar uma única voz pode ter um grande efeito em um grafo de áudio.

## <a name="to-dynamically-change-an-audio-graph"></a>Para alterar dinamicamente um grafo de áudio

Adicionar e remover vozes de um grafo de áudio é muito semelhante a adicionar ou remover nós de uma única lista ou grafo vinculado.

-   Para adicionar uma voz ou um subgrafo a um grafo de áudio

    Defina a saída de uma voz no grafo, a voz pai, para a voz a ser adicionada usando a função [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) . Defina a saída da nova voz para o filho original da voz pai.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   Para remover uma voz ou um subgrafo de um grafo de áudio

    Defina a voz de saída do pai da voz que está sendo removida para o filho da voz que está sendo removida. Se a voz que está sendo removida estiver no final do grafo, a voz pai deverá ser alterada para apontar para a voz mestra.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Observe que, para maior clareza, cada pai tem apenas um filho nesses exemplos. Se um nó pai tiver vários filhos, sua caixa de envio conterá uma matriz de vozes em vez de um ponteiro para apenas uma voz.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gráficos de áudio](audio-graphs.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Como: Usar vozes de submixagem](how-to--use-submix-voices.md)
</dt> <dt>

[Como: Criar uma cadeia de efeitos](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
