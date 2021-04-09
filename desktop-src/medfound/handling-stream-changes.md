---
description: Este tópico descreve como uma Media Foundation transformação (MFT) deve tratar as alterações de formato durante o streaming.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Manipulando alterações de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164844"
---
# <a name="handling-stream-changes"></a>Manipulando alterações de fluxo

Este tópico descreve como uma Media Foundation transformação (MFT) deve tratar as alterações de formato durante o streaming.

> [!IMPORTANT]
>
> Este tópico não se aplica a codificadores. Os codificadores não devem propagar alterações de formato conforme descrito neste tópico. Os codificadores devem aceitar apenas um tipo de entrada que corresponda ao tipo de saída atualmente configurado.

 

## <a name="overview-of-format-changes"></a>Visão geral das alterações de formato

Em geral, há dois motivos pelos quais um formato pode ser alterado durante o streaming.

-   O cliente pode mudar para um fluxo com um novo formato. Por exemplo, na televisão digital, isso pode ocorrer devido a uma alteração de canal.
-   Em alguns formatos de vídeo, como H. 264, o fragmentado pode sinalizar uma alteração de formato. Essas alterações podem incluir alterações no campo predominância, resolução de vídeo ou taxa de proporção de pixel.

Se o tipo de codificação for alterado, o cliente poderá precisar remover o MFT do pipeline e substituí-lo por outra MFT. (Por exemplo, o cliente pode precisar trocar um novo decodificador.) Este tópico não aborda essa situação. Este tópico aborda apenas o caso em que o MFT atual pode manipular o novo formato.

Se o formato for alterado, o MFT poderá exigir um novo tipo de entrada, um novo tipo de saída ou ambos.

-   As alterações no tipo de entrada são iniciadas pelo cliente. Um MFT nunca altera seu próprio tipo de entrada.
-   As alterações no tipo de saída são iniciadas pelo MFT. O MFT sinaliza que ele requer um novo tipo de saída, e o cliente negocia o novo tipo de saída com o MFT.

Assim, três casos distintos são possíveis:

-   O cliente define um novo tipo de entrada. O MFT consome o novo formato, sem alteração em seu tipo de saída.
-   O cliente define um novo tipo de entrada, e isso dispara uma alteração no tipo de saída.
-   O tipo de entrada não é alterado, mas o MFT detecta uma alteração de formato no fragmentado, que requer um novo tipo de saída.

## <a name="implementing-format-changes"></a>Implementando alterações de formato

O restante deste tópico descreve como o cliente deve processar uma alteração de formato e como implementar alterações de formato em um MFT.

### <a name="output-type"></a>Tipo de saída

Qualquer MFT pode iniciar uma alteração em seu tipo de saída, da seguinte maneira:

1.  O cliente chama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). O MFT responde da seguinte maneira:
    1.  O MFT não produz um exemplo de saída em [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  O MFT define o sinalizador de alteração do formato do buffer de dados de saída do MFT no membro **dwStatus** da estrutura do [**buffer de dados de saída da MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) . **\_ \_ \_ \_ \_**
    3.  O método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retorna o código de erro **MF \_ E \_ Transform \_ Stream \_ Change**.
2.  O cliente chama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Esse método retorna um conjunto atualizado de tipos de saída.
3.  O cliente chama [**Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir um novo tipo de saída.
4.  O cliente retoma a chamada de [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Tipo de entrada

As alterações no tipo de entrada são iniciadas pelo cliente, nunca pela MFT. Se o tipo de entrada for alterado, ele poderá disparar uma alteração no tipo de saída.

A sequência exata de eventos depende do valor do atributo de [**\_ alteração de \_ \_ formato dinâmico \_ de suporte de MFT**](mft-support-dynamic-format-change-attribute.md) .



| Valor     | Descrição                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Antes que o cliente defina um novo tipo de entrada, ele deve drenar o MFT. |
| **TRUE**  | O cliente pode definir um novo tipo de entrada sem descarregar o MFT.   |



 

Um MFT expõe esse atributo por meio de seu método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . O valor padrão desse atributo é **false**; Se o MFT não definir o atributo, trate o valor como **false**.

**O MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_ é falso**

1.  O cliente envia a mensagem de [**dreno do comando de mensagem do MFT \_ \_ \_**](mft-message-command-drain.md) .
2.  O cliente drena o MFT chamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) até que **ProcessOutput** retorne **MF \_ E \_ transformação \_ precisam de \_ mais \_ entradas**.
3.  O cliente chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o novo tipo de entrada.
4.  O MFT valida o tipo de entrada. Se o tipo for inválido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) retornará **MF \_ E \_ INVALIDMEDIATYPE** ou outro código de erro. Caso contrário, **SetInputType** retornará S \_ OK.
5.  Supondo que o tipo de entrada seja válido, o MFT avalia se o tipo de saída também é alterado. Caso contrário, o streaming continuará e nenhuma ação adicional será necessária.
6.  Se o tipo de saída for alterado:
    1.  O MFT invalida seu tipo de mídia de saída atual e atualiza a lista de tipos de mídia de saída disponíveis.
    2.  A próxima chamada para [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retorna **a \_ \_ alteração do \_ fluxo \_ de MF e de transformação**, conforme descrito na seção anterior.
    3.  O cliente chama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista atualizada de tipos de saída.
    4.  O cliente chama [**Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

**O MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_ é verdadeiro**

1.  O cliente chama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o novo tipo de entrada.
2.  O MFT valida o tipo de entrada. Se o tipo for inválido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) retornará **MF \_ E \_ INVALIDMEDIATYPE** ou outro código de erro. Caso contrário, **SetInputType** retornará S \_ OK.
3.  Supondo que o tipo de entrada seja válido, o MFT avalia se o tipo de saída também é alterado. Caso contrário, o streaming continuará e nenhuma ação adicional será necessária.
4.  Antes que o tipo de saída seja alterado, o MFT deve processar qualquer amostra de entrada armazenada em cache, da seguinte maneira:
    1.  O MFT não invalida seu tipo de saída atual.
    2.  O MFT produz o máximo de saída possível dos exemplos de entrada em cache.
    3.  É opcional se o MFT aceita novos exemplos de entrada enquanto processa as amostras armazenadas em cache. Nesse caso, os novos exemplos de entrada usarão o novo formato de entrada, de modo que o MFT deve manter o controle do ponto quando o formato for alterado.
5.  Depois que o MFT processa todos os exemplos recebidos antes do tipo de entrada alterado, o [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retorna **MF \_ E \_ Transform \_ Stream \_ Change**.
6.  O MFT invalida seu tipo de saída atual e atualiza a lista de tipos de mídia de saída disponíveis.
7.  O cliente negocia o novo tipo de saída, conforme descrito anteriormente.

O [MFTs assíncrono](asynchronous-mfts.md) deve retornar o valor **true** para o atributo de [**\_ \_ \_ \_ alteração de formato dinâmico de suporte de MFT**](mft-support-dynamic-format-change-attribute.md) . Ao usar uma MFT assíncrona, o cliente pode assumir que o atributo de **\_ \_ \_ \_ alteração de formato dinâmico de suporte de MFT** está definido como **true**.

Quando o [**MFT \_ dá suporte à \_ \_ \_ alteração de formato dinâmico**](mft-support-dynamic-format-change-attribute.md) é **verdadeiro**, a principal diferença é que o cliente não precisa drenar o MFT antes de definir um novo tipo de entrada. Como resultado, o tipo de entrada pode mudar enquanto o MFT estiver mantendo os exemplos de entrada. É importante que o MFT não simplesmente descarte esses exemplos. Além disso, o tipo de saída não pode ser alterado até que o MFT processe todos os seus dados armazenados em cache.

O parágrafo anterior se aplica especialmente a decodificadores de vídeo, que podem receber quadros embutidos fora da ordem temporal e, portanto, precisam armazená-los em cache. Se uma MFT não armazenar amostras de entrada em cache, o descarregamento é essencialmente um não op. Nesse caso, o MFT pode definir a [**\_ alteração de \_ \_ formato dinâmico \_ do suporte de MFT**](mft-support-dynamic-format-change-attribute.md) para **false** (ou deixar a definição do atributo).

Além disso, observe que cada MFT é esperado para tratar as alterações de formato corretamente após serem descarregadas. O atributo de [**\_ \_ \_ \_ alteração de formato dinâmico de suporte de MFT**](mft-support-dynamic-format-change-attribute.md) indica se o MFT dá suporte a alterações de formato sem drenagem.

## <a name="change-in-interlace-mode"></a>Alterar no modo de entrelaçamento

As alterações no modo de entrelaçamento de vídeo são um caso especial, porque não invalidam o tipo de mídia atual. Em vez disso, o modo de entrelaçamento é especificado para cada quadro de vídeo definindo atributos no exemplo de mídia. Um MFT de vídeo deve verificar cada exemplo de entrada para a presença desses sinalizadores.

O modo de entrelaçamento pode ser alterado quando o campo predominância alterna do campo de cima para baixo, ou quando o vídeo alterna entre imagens progressivas e entrelaçadas.

Para obter mais informações, consulte os [sinalizadores de entrelaçamento em exemplos](video-interlacing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



