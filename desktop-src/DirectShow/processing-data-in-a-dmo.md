---
description: Processando dados em um DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Processando dados em um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825834"
---
# <a name="processing-data-in-a-dmo"></a>Processando dados em um DMO

Esta seção explica como processar um fluxo de dados usando um DMO. As etapas listadas nesta seção são o comportamento padrão; todos os DMOs devem dar suporte aos métodos descritos aqui. Esses métodos usam buffers separados para entrada e saída. Alguns DMOs também dão suporte ao processamento in-loco, usando um único buffer. Para obter mais informações sobre o processamento in-loco, consulte [processamento](in-place-processing.md)in-loco.

**Alocando buffers**

O cliente é responsável por toda a alocação de buffer. Depois de definir os tipos de mídia no DMO, consulte os requisitos de buffer do DMO para cada fluxo. Eles podem mudar dependendo do tipo de mídia. Para cada fluxo, chame o método [**IMediaObject:: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) ou [**IMediaObject:: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Esses métodos retornam as seguintes informações:

-   Tamanho mínimo do buffer, em bytes.
-   Requisitos de alinhamento, se houver. Um buffer será alinhado se o endereço inicial for um múltiplo de algum número inteiro especificado.
-   A quantidade máxima de dados que o DMO manterá para o lookahead. Esse número se aplica somente a fluxos de entrada. Para alguns tipos de dados (por exemplo, codificação MPEG), um DMO pode precisar olhar para a frente no fluxo. O valor de lookahead indica a quantidade de dados de entrada que o DMO precisará antes de produzir a saída.

O cliente deve alocar buffers que correspondam a esses requisitos. Além disso, o DMO pode ter requisitos sobre como o cliente empacota os dados de entrada. Por exemplo, o DMO pode exigir que cada buffer contenha exatamente um exemplo (ou quadro de vídeo). Para determinar esses requisitos, chame o método [**IMediaObject:: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . O método [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) retorna informações semelhantes sobre um fluxo de saída.

No modelo de streaming padrão, o cliente não passa ponteiros de buffer brutos para o DMO. Em vez disso, ele usa um objeto COM leve que expõe a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . A interface **IMediaBuffer** age como um wrapper com para um bloco de memória. Como ele é um objeto COM, ele dá suporte à contagem de referência, o que ajuda a garantir que os buffers não sejam liberados enquanto ainda estiverem em uso.

> [!Note]  
> A interface **IMediaBuffer** serve uma função semelhante à interface **IMediaSample** no DirectShow.

 

O cliente deve implementar o objeto **IMediaBuffer** . Para obter mais informações, consulte [Implementing IMediaBuffer](implementing-imediabuffer.md).

**Processando os dados**

Para processar dados, faça o seguinte:

1.  Para cada fluxo de entrada, preencha um buffer com dados de entrada.
2.  Chame [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) para entregar cada buffer.
3.  Chame [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) para processar os dados. Esse método usa uma matriz de buffers, uma para cada fluxo de saída.
4.  Repita até que não haja mais dados de entrada.

O método **ProcessInput** aceita a entrada para um fluxo de cada vez. Normalmente, o método retorna imediatamente e o DMO mantém uma contagem de referência no objeto **IMediaBuffer** . Ele libera o objeto depois de processar todos os dados no buffer ou quando o aplicativo libera o DMO. Não use novamente um buffer até que o DMO o tenha liberado. Para determinar se um fluxo de entrada pode aceitar mais dados, chame o método [**IMediaObject:: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . Esse método retornará o \_ sinalizador de entrada de dados STATUSF Input do DMO \_ \_ \_ se o fluxo puder aceitar mais entradas.

O método **ProcessOutput** gera a saída para todos os fluxos de saída de uma vez. O aplicativo passa em uma matriz de estruturas de buffer de dados de saída de DMO, uma para cada fluxo de saída. [**\_ \_ \_**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) Cada estrutura na matriz tem um ponteiro para um objeto **IMediaBuffer** . O DMO grava tantos dados de saída quanto podem nos buffers. Ele também define vários sinalizadores para relatar o status da operação. O \_ sinalizador incompleto de dados de saída do DMO \_ \_ \_ indica que o DMO pode produzir mais resultados da entrada existente. Nesse caso, o cliente pode chamar **ProcessOutput** novamente. Caso contrário, ele deve chamar **ProcessInput** com mais dados de entrada. O DMO nunca modifica os dados nos buffers de entrada; Ele grava somente nos buffers de saída.

Depois de entregar todos os dados a um fluxo de entrada, chame o método [**IMediaObject::D iscontinuion**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . O DMO não aceita outras entradas para esse fluxo até que você processe a saída restante (ou libere o DMO).

A qualquer momento depois que o streaming começa, o DMO é capaz de receber entrada ou produzir saída, ou ambos. Portanto, **GetInputStatus** retorna a \_ entrada DMO \_ STATUSF \_ aceita \_ dados, ou **ProcessOutput** retorna DMO \_ dados de saída \_ \_ BUFFERF \_ incompletos. O aplicativo mantém os dados fluindo para esses sinalizadores e chamando **ProcessInput** ou **ProcessOutput** de acordo. Para interromper o fluxo de dados, chame o método [**IMediaObject:: flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . Esse método faz com que o DMO descarte todos os buffers que está segurando internamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Processamento in-loco](in-place-processing.md)
</dt> </dl>

 

 



