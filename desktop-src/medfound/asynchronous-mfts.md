---
description: Este tópico descreve o processamento de dados assíncronos para transformações de Media Foundation (MFTs).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFTs assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cab2ef683ef22fd22a911c045a1a744f1c0d561b3e8e66d46ca2cf6c6f0ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959516"
---
# <a name="asynchronous-mfts"></a>MFTs assíncrona

Este tópico descreve o processamento de dados assíncronos para transformações de Media Foundation (MFTs).

> [!Note]  
> este tópico aplica-se ao Windows 7 ou posterior.

 

-   [Sobre MFTs assíncronas](#about-asynchronous-mfts)
-   [Requisitos gerais](#general-requirements)
-   [Eventos](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Drenagem](#draining)
-   [Liberação](#flushing)
-   [Marcadores](#markers)
-   [Alterações de formato](#format-changes)
-   [Atributos](#attributes)
-   [Desbloqueando MFTs assíncronas](#unlocking-asynchronous-mfts)
-   [Desligando o MFT](#shutting-down-the-mft)
-   [Registro e enumeração](#registration-and-enumeration)
-   [Tópicos relacionados](#related-topics)

## <a name="about-asynchronous-mfts"></a>Sobre MFTs assíncronas

quando MFTs foram introduzidos no Windows Vista, a API foi projetada para o processamento de dados *síncrono* . Nesse modelo, a MFT está sempre esperando para obter entrada ou aguardando para produzir a saída.

Considere um decodificador de vídeo típico. Para obter um quadro decodificado, o cliente chama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se o decodificador tiver dados suficientes para decodificar um quadro, o **ProcessOutput** será bloqueado enquanto o MFT decodificar o quadro. Caso contrário, **ProcessOutput** retornará **MF_E_TRANSFORM_NEED_MORE_INPUT**, indicando que o cliente deve chamar [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Esse modelo funciona bem se o decodificador executa todas as suas operações de decodificação em um thread. Mas suponha que o decodificador use vários threads para decodificar quadros em paralelo. Para obter o melhor desempenho, o decodificador deve receber nova entrada sempre que um thread de decodificação se tornar ocioso. Mas a taxa em que os threads concluíram as operações de decodificação não serão alinhadas exatamente às chamadas do cliente para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), resultando em threads aguardando o trabalho.

Windows 7 introduz o processamento *assíncrono* controlado por eventos para MFTs. Nesse modelo, sempre que o MFT precisa de entrada ou tem saída, ele envia um evento para o cliente.

## <a name="general-requirements"></a>Requisitos gerais

Este tópico descreve como o MFTs assíncrono difere do MFT síncrono. Exceto quando indicado neste tópico, os dois modelos de processamento são os mesmos. (Em particular, a negociação de formato é a mesma.)

Uma MFT assíncrona deve implementar as seguintes interfaces:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Eventos

Um MFT assíncrono usa os seguintes eventos para sinalizar seu status de processamento de dados:



| Evento                                                    | Descrição                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Enviado quando o MFT pode aceitar mais entradas.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Enviado quando o MFT tem saída.                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Enviado quando uma operação de descarga é concluída. Consulte [drenagem](#draining). |
| [METransformMarker](metransformmarker.md)               | Enviado quando um marcador é processado. Consulte [marcadores](#markers).           |



 

Esses eventos são enviados fora de banda. É importante entender a diferença entre eventos em banda e fora de banda no contexto de uma MFT.

O design de MFT original dá suporte a eventos *em banda* . Um evento em banda contém informações sobre o fluxo de dados, como informações sobre uma alteração de formato. O cliente envia eventos em banda para o MFT chamando [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). O MFT pode enviar eventos em banda de volta para o cliente no método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . (Especificamente, os eventos são transmitidos no membro **pEvents** da estrutura [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .)

Uma MFT envia eventos fora de banda por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da seguinte maneira:

1.  O MFT implementa a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , conforme descrito em [geradores de eventos de mídia](media-event-generators.md).
2.  O cliente chama **IUnknown:: QueryInterface** no MFT para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Uma MFT assíncrona deve expor essa interface. O MFTs síncrono não deve expor essa interface.
3.  O cliente chama [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) e [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para receber eventos fora de banda do MFT.

## <a name="processinput"></a>ProcessInput

O método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) é modificado da seguinte maneira:

1.  Quando o streaming é iniciado, o cliente envia a mensagem de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
2.  Durante o streaming, o MFT solicita dados enviando um evento [METransformNeedInput](metransformneedinput.md) . Os dados do evento são o identificador de fluxo.
3.  Para cada evento [METransformNeedInput](metransformneedinput.md) , o cliente chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para o fluxo especificado.
4.  No final do streaming, o cliente pode chamar [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .

Notas de implementação:

-   O MFT não deve enviar nenhum evento [METransformNeedInput](metransformneedinput.md) até receber a mensagem de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
-   Durante o streaming, o MFT pode enviar eventos [METransformNeedInput](metransformneedinput.md) a qualquer momento.
-   O MFT deve manter uma contagem de eventos [METransformNeedInput](metransformneedinput.md) pendentes. Qualquer chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) que não corresponde a um evento METransformNeedInput deve retornar **MF_E_NOTACCEPTING**.
-   Quando o MFT recebe a mensagem de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) , ele redefine a contagem de eventos [METransformNeedInput](metransformneedinput.md) pendentes para zero.
-   A MFT não deve enviar nenhum evento [METransformNeedInput](metransformneedinput.md) depois que receber a mensagem de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .
-   Se [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) for chamado antes de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) ou depois de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), o método deverá retornar **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

O método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) é modificado da seguinte maneira:

1.  Sempre que o MFT tiver saída, ele enviará um evento [METransformHaveOutput](metransformhaveoutput.md) .
2.  Para cada evento [METransformHaveOutput](metransformhaveoutput.md) , o cliente chama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Notas de implementação:

-   Se o cliente chamar [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) a qualquer outro momento, o método retornará **E_UNEXPECTED**.
-   Um MFT assíncrono nunca deve retornar **MF_E_TRANSFORM_NEED_MORE_INPUT** do método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Se o MFT exigir mais entrada, ele enviará um evento [METransformNeedInput](metransformneedinput.md) .

## <a name="draining"></a>Drenagem

O descarregamento de uma MFT faz com que o MFT produza o máximo de saída possível de qualquer dado de entrada já enviado. O descarregamento de um MFT assíncrono funciona da seguinte maneira:

1.  O cliente envia a mensagem de [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) .
2.  O MFT continua enviando eventos [METransformHaveOutput](metransformhaveoutput.md) até que não haja mais dados a serem processados. Ele não envia eventos [METransformNeedInput](metransformneedinput.md) durante esse tempo.
3.  Depois que o MFT envia o último evento [METransformHaveOutput](metransformhaveoutput.md) , ele envia um evento [METransformDrainComplete](metransformdraincomplete.md) .

Após a conclusão do descarregamento, o MFT não envia outro evento [METransformNeedInput](metransformneedinput.md) até receber uma mensagem de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) do cliente.

## <a name="flushing"></a>Liberação

O cliente pode liberar o MFT enviando a mensagem de [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) . O MFT descarta todos os exemplos de entrada e saída que ele está mantendo.

O MFT não envia outro [evento METransformNeedInput](metransformneedinput.md) até receber uma [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) do cliente.

## <a name="markers"></a>Marcadores

O cliente pode marcar um ponto no fluxo enviando a [**mensagem MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) dados. O MFT responde da seguinte forma:

1.  O MFT gera o máximo de amostras de saída possível dos dados de entrada existentes, enviando um [evento METransformHaveOutput](metransformhaveoutput.md) para cada exemplo de saída.
2.  Depois que toda a saída é gerada, o MFT envia um [evento METransformMarker.](metransformmarker.md) Esse evento deve ser enviado após todos os eventos [METransformHaveOutput.](metransformhaveoutput.md)

Por exemplo, suponha que um decodificador tenha dados de entrada suficientes para produzir quatro exemplos de saída. Se o cliente enviar a [**mensagem MFT_MESSAGE_COMMAND_MARKER,**](mft-message-command-marker.md) o MFT colocará quatro eventos [METransformHaveOutput](metransformhaveoutput.md) em fila (um por exemplo de saída), seguidos por um evento [METransformMarker.](metransformmarker.md)

A mensagem de marcador é semelhante à mensagem de dreno. No entanto, um dreno é considerado uma quebra no fluxo, enquanto um marcador não é. O esvaziamento e os marcadores têm as seguintes diferenças.

Drenagem:

-   Durante o esgotamento, o MFT não envia [eventos METransformNeedInput.](metransformneedinput.md)
-   O MFT descarta todos os dados de entrada que não podem ser usados para criar um exemplo de saída.
-   Alguns MFTs produzem uma "cauda" no final dos dados. Por exemplo, efeitos de áudio, como reverb ou echo, produzem dados extras depois que os dados de entrada são interrompidos. Uma MFT que gera uma cauda deve fazer isso no final de uma operação de esgotamento.
-   Depois que o MFT terminar de esvaziar, ele marca a próxima amostra de saída com o atributo [**MFSampleExtension_Discontinuity,**](mfsampleextension-discontinuity-attribute.md) para indicar uma descontinuidade no fluxo.

Marcador:

-   O MFT continua a enviar [eventos METransformNeedInput](metransformneedinput.md) antes de enviar o evento de marcador.
-   O MFT não descarta nenhum dado de entrada. Se houver dados parciais, eles deverão ser processados após o ponto de marcador.
-   O MFT não produz uma cauda no ponto de marcador.
-   O MFT não configura o sinalizador de descontinuidade após o ponto de marcador.

## <a name="format-changes"></a>Alterações de formato

Um MFT assíncrono deve dar suporte a alterações de formato dinâmico, conforme descrito em [Manipulando alterações de fluxo.](handling-stream-changes.md)

## <a name="attributes"></a>Atributos

Um MFT assíncrono deve implementar o método [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para retornar um armazenamento de atributos válido. Os seguintes atributos se aplicam a MFTs assíncronos:



| Atributo                                                                                    | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | O MFT deve definir esse atributo **como TRUE** (1). O cliente pode consultar esse atributo para descobrir se o MFT é assíncrono. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | O MFT deve definir esse atributo **como TRUE** (1). O cliente pode assumir que esse atributo está definido.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Desbloqueando MFTs assíncronos

Os MFTs assíncronos não são compatíveis com o modelo de processamento de dados MFT original. Para impedir que os MFTs assíncronos quebrando aplicativos existentes, o seguinte mecanismo é definido:

<dl> O cliente chama <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform::GetAttributes</a> no MFT.  
O cliente consulta o para este <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> atributo. Para um MFT assíncrono, o valor desse atributo é **TRUE.**  
Para desbloquear o MFT, o cliente deve define o <a href="mf-transform-async-unlock.md">atributo MF_TRANSFORM_ASYNC_UNLOCK</a> como **TRUE.**  
</dl>

Até que o cliente desbloqueie o MFT, todos os métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) deverão retornar MF_E_TRANSFORM_ASYNC_LOCKED **,** com as seguintes exceções:

-   [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (todos os MFTs assíncronos)
-   [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (todos os MFTs assíncronos)
-   [**IMFTransform::GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (somente codificadores)
-   [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (somente codificadores)
-   [**IMFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (todos os MFTs assíncronos)
-   [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (todos os MFTs assíncronos)

O código a seguir mostra como desbloquear um MFT assíncrono:


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Desligando o MFT

Os MFTs assíncronos devem implementar a interface [**IMFShutdown.**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

-   [**Desligamento:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)o MFT deve desligar sua fila de eventos. Se estiver usando a fila de eventos padrão, chame [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Opcionalmente, o MFT pode liberar outros recursos. O cliente não deve usar o MFT depois de chamar **Desligamento**.
-   [**GetShutdownStatus:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)depois que [**o**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) desligamento tiver sido chamado, o MFT deverá retornar o valor **MFSHUTDOWN_COMPLETED** no parâmetro *pStatus.* Ele não deve retornar o valor **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Registro e enumeração

Para registrar um MFT assíncrono, chame a [**função MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) e de definido o sinalizador **MFT_ENUM_FLAG_ASYNCMFT** no *parâmetro Flags.* (Anteriormente, esse sinalizador era reservado.)

Para enumerar MFTs assíncronos, chame a [**função MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e de definido o sinalizador **MFT_ENUM_FLAG_ASYNCMFT** no *parâmetro Flags.* Para compatibilidade com backward, a [**função MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) não enumera MFTs assíncronos. Caso contrário, instalar um MFT assíncrono no computador do usuário pode quebrar os aplicativos existentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 



