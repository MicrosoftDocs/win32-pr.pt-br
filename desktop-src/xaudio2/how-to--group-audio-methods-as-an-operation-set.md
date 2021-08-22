---
description: Este tópico mostra como você pode agrupar os métodos XAudio2 para que eles entrem em vigor ao mesmo tempo.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Como: Agrupar métodos de áudio como um conjunto de operações'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f5c1d27e33db4c0f7910761a7be574b72e9ac7aaa91b14329fa003792860d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082920"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Como: Agrupar métodos de áudio como um conjunto de operações

Este tópico mostra como você pode agrupar os métodos XAudio2 para que eles entrem em vigor ao mesmo tempo.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Para agrupar métodos de áudio como um conjunto de operações

1.  Declare um contador de conjunto de operações globais.

    O contador de [conjunto de operações](operation-sets.md) garante que cada conjunto de operações seja exclusivo.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Incrementar o contador global.

    Cada vez que você envia um novo [conjunto de operações](operation-sets.md), o contador global deve ser incrementado para garantir que cada conjunto seja exclusivo.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Agrupe as chamadas de método definindo seus parâmetros de [conjunto de operações](operation-sets.md) .

4.  Defina os parâmetros do [conjunto de operações](operation-sets.md) como o valor atual do contador global.

    Nesse caso, quatro chamadas para [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) são agrupadas como uma [operação definida](operation-sets.md). O agrupamento das chamadas faz com que todos os quatro sons sejam iniciados exatamente ao mesmo tempo.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Inicie o [conjunto de operações](operation-sets.md).

    Depois de chamar todos os métodos no conjunto, inicie o conjunto chamando [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com o valor atual do contador global.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de operações](operation-sets.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Conjuntos de operações XAudio2](xaudio2-operation-sets.md)
</dt> </dl>

 

 
