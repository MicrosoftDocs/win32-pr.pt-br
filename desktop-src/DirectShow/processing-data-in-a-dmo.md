---
description: Processando dados em um DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Processando dados em um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd4dd05df960bd27b34eb55b604c8469e7bbaedd57ea928f5b4f412ad4bff04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748236"
---
# <a name="processing-data-in-a-dmo"></a>Processando dados em um DMO

Esta seção explica como processar um fluxo de dados usando um DMO. As etapas listadas nesta seção são o comportamento padrão; todos os DMOs devem dar suporte aos métodos descritos aqui. Esses métodos usam buffers separados para entrada e saída. Alguns DMOs também dão suporte ao processamento in-loco, usando um único buffer. Para obter mais informações sobre o processamento in-loco, consulte [processamento](in-place-processing.md)in-loco.

**Alocando buffers**

O cliente é responsável por toda a alocação de buffer. depois de definir os tipos de mídia no DMO, consulte a DMO para obter os requisitos de buffer de cada fluxo. Eles podem mudar dependendo do tipo de mídia. Para cada fluxo, chame o método [**IMediaObject:: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) ou [**IMediaObject:: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Esses métodos retornam as seguintes informações:

-   Tamanho mínimo do buffer, em bytes.
-   Requisitos de alinhamento, se houver. Um buffer será alinhado se o endereço inicial for um múltiplo de algum número inteiro especificado.
-   a quantidade máxima de dados que o DMO será mantido para antecipação. Esse número se aplica somente a fluxos de entrada. para alguns tipos de dados (por exemplo, codificação MPEG), talvez seja necessário examinar uma DMO no fluxo. o valor de lookahead indica a quantidade de dados de entrada que o DMO exigirá antes que possa produzir a saída.

O cliente deve alocar buffers que correspondam a esses requisitos. além disso, o DMO pode ter requisitos sobre como o cliente empacota os dados de entrada. por exemplo, a DMO pode exigir que cada buffer contenha exatamente um exemplo (ou quadro de vídeo). Para determinar esses requisitos, chame o método [**IMediaObject:: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . O método [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) retorna informações semelhantes sobre um fluxo de saída.

No modelo de streaming padrão, o cliente não passa ponteiros de buffer brutos para a DMO. Em vez disso, ele usa um objeto COM leve que expõe a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . A interface **IMediaBuffer** age como um wrapper com para um bloco de memória. Como ele é um objeto COM, ele dá suporte à contagem de referência, o que ajuda a garantir que os buffers não sejam liberados enquanto ainda estiverem em uso.

> [!Note]  
> A interface **IMediaBuffer** serve uma função semelhante à interface **IMediaSample** no DirectShow.

 

O cliente deve implementar o objeto **IMediaBuffer** . Para obter mais informações, consulte [Implementing IMediaBuffer](implementing-imediabuffer.md).

**Processando os dados**

Para processar dados, faça o seguinte:

1.  Para cada fluxo de entrada, preencha um buffer com dados de entrada.
2.  Chame [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) para entregar cada buffer.
3.  Chame [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) para processar os dados. Esse método usa uma matriz de buffers, uma para cada fluxo de saída.
4.  Repita até que não haja mais dados de entrada.

O método **ProcessInput** aceita a entrada para um fluxo de cada vez. normalmente, o método retorna imediatamente e o DMO mantém uma contagem de referência no objeto **IMediaBuffer** . Ele libera o objeto depois de processar todos os dados no buffer ou quando o aplicativo libera o DMO. não reutilize um buffer até que o DMO o tenha liberado. Para determinar se um fluxo de entrada pode aceitar mais dados, chame o método [**IMediaObject:: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . esse método retorna o \_ sinalizador de dados de STATUSF de entrada de aceitação DMO \_ \_ \_ se o fluxo pode aceitar mais entradas.

O método **ProcessOutput** gera a saída para todos os fluxos de saída de uma vez. o aplicativo passa em uma matriz de [**DMO estruturas de BUFFER de \_ \_ dados \_ de saída**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) , uma para cada fluxo de saída. Cada estrutura na matriz tem um ponteiro para um objeto **IMediaBuffer** . a DMO grava tantos dados de saída quanto podem nos buffers. Ele também define vários sinalizadores para relatar o status da operação. o \_ sinalizador incompleto de dados de saída do DMO \_ \_ BUFFERF \_ indica que o DMO pode produzir mais resultados da entrada existente. Nesse caso, o cliente pode chamar **ProcessOutput** novamente. Caso contrário, ele deve chamar **ProcessInput** com mais dados de entrada. o DMO nunca modifica os dados nos buffers de entrada; Ele grava somente nos buffers de saída.

Depois de entregar todos os dados a um fluxo de entrada, chame o método [**IMediaObject::D iscontinuion**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . o DMO não aceita outras entradas para esse fluxo até que você processe a saída restante (ou libere a DMO).

a qualquer momento depois que o streaming começa, o DMO é capaz de receber entrada ou produzir saída, ou ambos. portanto, o **GetInputStatus** retorna DMO \_ entrada \_ STATUSF \_ aceitar \_ dados ou **ProcessOutput** retorna DMO \_ dados de \_ saída \_ BUFFERF \_ incompletos. O aplicativo mantém os dados fluindo para esses sinalizadores e chamando **ProcessInput** ou **ProcessOutput** de acordo. Para interromper o fluxo de dados, chame o método [**IMediaObject:: flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . esse método faz com que o DMO descarte os buffers que estão em manutenção internamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Processamento in-loco](in-place-processing.md)
</dt> </dl>

 

 



