---
description: Media Foundation transformação (MFTs) são uma evolução do modelo de transformação introduzido pela primeira vez com DMOs (Objetos de Mídia DirectX).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Comparação de MFTs e DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958976"
---
# <a name="comparison-of-mfts-and-dmos"></a>Comparação de MFTs e DMOs

Media Foundation transformação (MFTs) são uma evolução do modelo de transformação introduzido pela primeira vez com DMOs (Objetos de Mídia DirectX). Este tópico resume as principais maneiras pelas quais os MFTs diferem dos DMOs. Leia este tópico se você já estiver familiarizado com as interfaces DMO ou se quiser converter um DMO existente em um MFT.

Este tópico contém as seguintes seções:

-   [Número de Fluxos](#number-of-streams)
-   [Negociação de formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Alocando recursos](#allocating-resources)
    -   [Processando dados](#processing-data)
    -   [Liberando](#flushing)
    -   [Descontinuidades do fluxo](#stream-discontinuities)
-   [Diferenças diversas](#miscellaneous-differences)
-   [Sinalizadores](#flags)
    -   [Sinalizadores ProcessInput](#processinput-flags)
    -   [Sinalizadores ProcessOutput](#processoutput-flags)
    -   [Sinalizadores GetInputStatus](#getinputstatus-flags)
    -   [Sinalizadores GetOutputStatus](#getoutputstatus-flags)
    -   [Sinalizadores GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Sinalizadores GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Sinalizadores SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Códigos de Erro](#error-codes)
-   [Criando objetos DMO/MFT híbridos](#creating-hybrid-dmomft-objects)
-   [Tópicos relacionados](#related-topics)

## <a name="number-of-streams"></a>Número de Fluxos

Um DMO tem um número fixo de fluxos, enquanto um MFT pode dar suporte a um número dinâmico de fluxos. O cliente pode adicionar fluxos de entrada e o MFT pode adicionar novos fluxos de saída durante o processamento. No entanto, os MFTs não são necessários para dar suporte a fluxos dinâmicos. Uma MFT pode ter um número fixo de fluxos, assim como um DMO.

Os seguintes métodos são usados para dar suporte a fluxos dinâmicos em um MFT:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Além disso, o [**método IMFTransform::P rocessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) define o comportamento para adicionar ou remover fluxos de saída.

Como os DMOs têm fluxos fixos, os fluxos em um DMO são identificados usando valores de índice baseados em zero. Os MFTs, por outro lado, usam identificadores de fluxo que não correspondem necessariamente aos valores de índice. Isso porque o número de fluxos em um MFT pode mudar. Por exemplo, o fluxo 0 pode ser removido, deixando o fluxo 1 como o primeiro fluxo. No entanto, um MFT com um número fixo de fluxos deve observar a mesma convenção que os DMOs e usar valores de índice para identificadores de fluxo.

## <a name="format-negotiation"></a>Negociação de formato

Os MFTs usam a interface [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) para descrever tipos de mídia. Caso contrário, a negociação de formato com MFTs funciona com os mesmos princípios básicos que os DMOs. A tabela a seguir lista os métodos de negociação de formato para DMOs e os métodos correspondentes para MFTs.



| DMO método                                                                        | Método MFT                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Assim como os DMOs, os MFTs processam dados por meio de chamadas para os métodos [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Aqui estão as principais diferenças entre os processos DMO E MFT ao transmitir dados.

### <a name="allocating-resources"></a>Alocando recursos

Os MFTs não têm os métodos [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) e [**IMediaObject::FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) usados com DMOs. Para lidar com a alocação e a desalocação de recursos com eficiência, uma MFT pode responder às seguintes mensagens no método [**IMFTransform::P rocessMessage:**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage)

-   [**NOTIFICAÇÃO DE \_ MENSAGEM MFT \_ INICIAR \_ \_ STREAMING**](mft-message-notify-begin-streaming.md)
-   [**INÍCIO DO FLUXO \_ \_ DE \_ NOTIFICAÇÃO DE MENSAGEM \_ MFT \_**](mft-message-notify-start-of-stream.md)

Além disso, o cliente pode sinalizar o início e o fim de um fluxo chamando [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com as seguintes mensagens:

-   [**FIM DO FLUXO \_ \_ DE \_ NOTIFICAÇÃO DE MENSAGEM \_ MFT \_**](mft-message-notify-end-of-stream.md)
-   [**STREAMING FINAL \_ DE \_ NOTIFICAÇÃO \_ DE MENSAGEM MFT \_**](mft-message-notify-end-streaming.md)

Essas duas mensagens não têm nenhuma DMO equivalente.

### <a name="processing-data"></a>Processando dados

Os MFTs usam exemplos de mídia para manter dados de entrada e saída. Exemplos de mídia expõem a interface [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) e contêm os seguintes dados:

-   Carimbo de data/hora e duração.
-   Atributos que contêm informações por exemplo. Para ver uma lista de atributos, consulte [Atributos de exemplo.](sample-attributes.md)
-   Zero ou mais buffers de mídia. Cada buffer de mídia expõe a interface [**IMFMediaBuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)

A interface [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) é semelhante à interface DMO **IMediaBuffer.** Para acessar o buffer de memória subjacente, chame [**IMFMediaBuffer::Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Esse método é aproximadamente equivalente a [**IMediaBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) para DMOs.

Para dados de vídeo descompactados, um buffer de mídia também pode dar suporte à interface [**IMF2DBuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) Um MFT que processa vídeo descompactado (como entrada ou saída) deve estar preparado para usar a interface **IMF2DBuffer** se o buffer o expõe. Para obter mais informações, consulte [Buffers de vídeo descompactados.](uncompressed-video-buffers.md)

Media Foundation fornece algumas implementações padrão de [**IMFMediaBuffer,**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)portanto, geralmente não é necessário escrever sua própria implementação. Para criar um buffer DMO de um buffer Media Foundation, chame [**MFCreateLegacyMediaBufferOnMFMediaBuffer.**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer)

### <a name="flushing"></a>Liberando

Os MFTs não têm um [**método Flush.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) Para liberar uma MFT, chame [**IMFTransform::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem [**FLUSH do COMANDO DE MENSAGEM \_ \_ \_ MFT.**](mft-message-command-flush.md)

### <a name="stream-discontinuities"></a>Descontinuidades do fluxo

Os MFTs não têm um método [**Descontinuidade.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) Para sinalizar uma descontinuidade em um fluxo, de definir o atributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) no exemplo de entrada.

## <a name="miscellaneous-differences"></a>Diferenças diversas

Aqui estão algumas diferenças secundárias adicionais entre MFTs e DMOs.

-   Não há equivalentes de MFT para os seguintes DMO métodos:
    -   [**IMediaObject::Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   Os MFTs não são necessários para dar suporte à agregação.
-   Os MFTs são suportados por uma operação chamada *de descarregamento.* A finalidade do esgotamento é processar todos os dados que permanecem no MF, sem fornecer mais dados de entrada para o MFT (por exemplo, no final do fluxo). Para esvaziar uma MFT, chame [**IMFTransform::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem DRAIN do COMANDO DE MENSAGEM [**\_ \_ \_ MFT.**](mft-message-command-drain.md) Para obter mais informações, consulte [Modelo básico de processamento MFT](basic-mft-processing-model.md).
-   Os MFTs podem ter atributos, incluindo atributos por fluxo. Use os seguintes métodos para obter os atributos de um MFT:

    -   [**IMFTransform::GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   Os MFTs podem processar eventos. Para enviar um evento para um MFT, chame [**IMFTransform::P rocessEvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Um MFT pode enviar um evento para o cliente por meio do [**método ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Para obter mais informações, consulte [Modelo básico de processamento MFT](basic-mft-processing-model.md).

## <a name="flags"></a>Flags

As tabelas a seguir listam os vários DMO e seus equivalentes de MFT. Sempre que um DMO é mapeado diretamente para um sinalizador MFT, ambos os sinalizadores têm o mesmo valor numérico. No entanto, DMO sinalizadores não têm equivalentes exatos de MFT e vice-versa.

### <a name="processinput-flags"></a>Sinalizadores ProcessInput

DMOs: DMO [**\_ \_ de \_ \_ SINALIZADORES DE BUFFER \_ DE DADOS DE**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) ENTRADA.

MFTs: nenhuma enumeração equivalente.



| DMO sinalizador                                  | Sinalizador MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO PONTO \_ DE SINCRONIZAÇÃO \_ DE BUFFER DE DADOS DE \_ ENTRADA**  | Nenhum sinalizador equivalente. Em vez disso, de definido [**o atributo MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo. |
| **\_DMO TEMPO \_ DE BUFFER DE DADOS DE \_ \_ ENTRADA**       | Nenhum sinalizador equivalente. Em vez disso, [**chame IMFSample::SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) no exemplo.                                  |
| **\_DMO INPUT \_ DATA \_ BUFFERF \_ TIMELENGTH** | Nenhum sinalizador equivalente. Em vez disso, [**chame IMFSample::SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) no exemplo.                          |



 

### <a name="processoutput-flags"></a>Sinalizadores ProcessOutput

DMOs: DMO [**\_ \_ \_ SINALIZADORES DE SAÍDA \_ DO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) PROCESSO.

MFTs: [**\_ enumeração \_ MFT PROCESS \_ OUTPUT \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)



| DMO sinalizador                                            | Sinalizador MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_DMO PROCESSAR \_ DESCARTE DE SAÍDA QUANDO NÃO HÁ \_ \_ \_ \_ BUFFER** | **DESCARTE DE SAÍDA \_ \_ DO PROCESSO MFT QUANDO NÃO \_ HÁ \_ \_ \_ BUFFER** |



 

DMOs: DMO [**\_ DE SAÍDA DE \_ \_ \_ SINALIZADORES \_ DE BUFFER DE**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) DADOS.


MFTs: [**\_ enumeração MFT \_ OUTPUT DATA BUFFER \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)



| DMO sinalizador                                   | Sinalizador MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO PONTO \_ DE SINCRONIZAÇÃO \_ DO BUFFERF DE DADOS DE \_ SAÍDA**  | Nenhum sinalizador equivalente. Em vez disso, verifique o [**atributo MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo. |
| **\_DMO TEMPO DE \_ BUFFER DE DADOS DE \_ \_ SAÍDA**       | Nenhum sinalizador equivalente. Em vez disso, [**chame IMFSample::GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) no exemplo.                                        |
| **\_DMO BUFFER \_ DE DADOS DE SAÍDA \_ \_ TIMELENGTH** | Nenhum sinalizador equivalente. Em vez disso, [**chame IMFSample::GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) no exemplo.                                |
| **\_DMO BUFFER \_ DE DADOS DE SAÍDA \_ INCOMPLETO \_** | **BUFFER DE DADOS \_ DE SAÍDA \_ MFT \_ \_ INCOMPLETO**                                                                                                           |
| Nenhum sinalizador equivalente.                        | **ALTERAÇÃO NO FORMATO \_ DO BUFFER DE DADOS DE \_ \_ \_ SAÍDA DO \_ MFT**                                                                                                       |
| Nenhum sinalizador equivalente.                        | **FIM DO FLUXO \_ DE BUFFER DE DADOS DE \_ \_ \_ SAÍDA MFT \_**                                                                                                          |
| Nenhum sinalizador equivalente.                        | **BUFFER DE DADOS \_ DE SAÍDA \_ MFT SEM \_ \_ \_ EXEMPLO**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Sinalizadores GetInputStatus

DMOs: DMO **\_ \_ de \_ SINALIZADORES DE STATUS \_ DE** ENTRADA.

MFTs: [**\_ enumeração \_ MFT INPUT \_ STATUS \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)



| DMO sinalizador                              | Sinalizador MFT                             |
|---------------------------------------|--------------------------------------|
| **\_DMO STATUS \_ DE ENTRADAF \_ ACEITAR \_ DADOS** | **ACEITAR DADOS \_ DE STATUS DE ENTRADA \_ \_ DO \_ MFT** |



 

### <a name="getoutputstatus-flags"></a>Sinalizadores GetOutputStatus

DMOs: nenhuma enumeração equivalente.

MFTs: [**\_ enumeração \_ MFT OUTPUT \_ STATUS \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)



| DMO sinalizador            | Sinalizador MFT                               |
|---------------------|----------------------------------------|
| Nenhum sinalizador equivalente. | **EXEMPLO DE STATUS DE SAÍDA DO MFT \_ \_ \_ \_ PRONTO** |



 

### <a name="getinputstreaminfo-flags"></a>Sinalizadores GetInputStreamInfo

DMOs: DMO [**\_ \_ de \_ \_ SINALIZADORES DE INFORMAÇÕES \_ DE FLUXO DE**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) ENTRADA.

MFTs: [**\_ enumeração MFT \_ INPUT STREAM INFO \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)



| DMO sinalizador                                             | Sinalizador MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_DMO AMOSTRAS \_ INTEIRAS DO STREAMF \_ \_ DE ENTRADA**              | **EXEMPLOS INTEIROS DO \_ FLUXO DE \_ ENTRADA \_ \_ MFT**              |
| **\_DMO EXEMPLO \_ ÚNICO DE STREAMF DE ENTRADA \_ POR \_ \_ \_ BUFFER** | **AMOSTRA \_ ÚNICA POR BUFFER DO \_ \_ FLUXO DE \_ ENTRADA \_ \_ MFT** |
| **\_DMO TAMANHO DE \_ EXEMPLO FIXO DO STREAMF DE \_ \_ \_ ENTRADA**         | **TAMANHO FIXO DA AMOSTRA DO FLUXO DE ENTRADA \_ \_ \_ \_ \_ MFT**         |
| **\_DMO O \_ STREAMF DE \_ ENTRADA CONTÉM \_ BUFFERS**              | **O FLUXO \_ DE \_ ENTRADA MFT CONTÉM \_ \_ BUFFERS**              |
| Nenhum sinalizador equivalente.                                  | **O FLUXO \_ DE \_ ENTRADA \_ MFT NÃO \_ \_ ADICIONA**           |
| Nenhum sinalizador equivalente.                                  | **FLUXO DE ENTRADA MFT \_ \_ \_ REMOVÍVEL**                   |
| Nenhum sinalizador equivalente.                                  | **FLUXO DE \_ ENTRADA MFT \_ \_ OPCIONAL**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Sinalizadores GetOutputStreamInfo

DMOs: DMO [**\_ \_ SINALIZADORES DE \_ INFORMAÇÕES DE FLUXO \_ \_ DE**](/previous-versions/ms806053(v=msdn.10)) SAÍDA.

MFTs: [**\_ enumeração \_ MFT OUTPUT \_ STREAM INFO \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)



| DMO sinalizador                                              | Sinalizador MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_DMO EXEMPLOS \_ INTEIROS DO STREAMF \_ \_ DE SAÍDA**              | **EXEMPLOS \_ \_ INTEIROS DO FLUXO DE \_ SAÍDA \_ MFT**              |
| **\_DMO EXEMPLO \_ ÚNICO DE STREAMF DE SAÍDA \_ POR \_ \_ \_ BUFFER** | **AMOSTRA \_ ÚNICA POR BUFFER DO \_ \_ FLUXO DE \_ SAÍDA \_ \_ MFT** |
| **\_DMO TAMANHO DE \_ EXEMPLO FIXO DO STREAMF DE \_ \_ \_ SAÍDA**         | **TAMANHO FIXO DA AMOSTRA \_ DE \_ FLUXO DE \_ \_ SAÍDA MFT \_**         |
| **\_DMO STREAMF \_ DE SAÍDA \_ DESCARTÁVEL**                 | **FLUXO DE \_ SAÍDA MFT \_ \_ DESCARTÁVEL**                 |
| **\_DMO STREAMF \_ DE \_ SAÍDA OPCIONAL**                    | **FLUXO DE SAÍDA \_ MFT \_ \_ OPCIONAL**                    |
| Nenhum sinalizador equivalente.                                   | **O FLUXO \_ DE SAÍDA \_ MFT FORNECE \_ \_ EXEMPLOS**           |
| Nenhum sinalizador equivalente.                                   | **O FLUXO DE SAÍDA DO MFT \_ \_ PODE FORNECER \_ \_ \_ EXEMPLOS**       |
| Nenhum sinalizador equivalente.                                   | **LEITURA LENTO \_ DO FLUXO DE SAÍDA \_ \_ MFT \_**                  |
| Nenhum sinalizador equivalente.                                   | **FLUXO DE SAÍDA MFT \_ \_ \_ REMOVÍVEL**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Sinalizadores SetInputType/SetOutputType

DMOs: DMO [**\_ \_ \_ enumeração SET TYPE \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)

MFTs: [**\_ enumeração \_ MFT SET \_ TYPE \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)



| DMO sinalizador                        | Sinalizador MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **\_DMO DEFINIR \_ SOMENTE TESTE DO TYPEF \_ \_** | **MFT \_ SET \_ TYPE \_ TEST \_ ONLY**                                                       |
| **\_DMO SET \_ TYPEF \_ CLEAR**      | Nenhum sinalizador equivalente. Em vez disso, de definir o tipo de mídia **como NULL** para limpar o tipo de mídia. |



 

## <a name="error-codes"></a>Códigos de erro

A tabela a seguir mostra como mapear DMO códigos de erro para códigos de erro MFT. Um objeto MFT/DMO híbrido deve retornar os códigos de erro DMO dos métodos [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e os códigos de erro MFT dos métodos [**IMFTransform.**](/windows/win32/api/mftransform/nn-mftransform-imftransform) Os DMO de erro são definidos no arquivo de header MediaErr.h. Os códigos de erro MFT são definidos no arquivo de header mferror.h.



| DMO código de erro                  | Código de erro MFT                       |
|---------------------------------|--------------------------------------|
| **\_DMO E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **\_DMO E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **\_DMO E \_ NOTACCEPTING**        | **MF \_ E \_ NOTACCEPTING**              |
| **\_DMO E \_ NÃO HÁ MAIS \_ \_ ITENS**     | **MF \_ E NÃO HÁ MAIS \_ \_ \_ TIPOS**           |
| **\_DMO E \_ TYPE \_ NOT \_ ACCEPTED** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_DMO E \_ TYPE \_ NOT \_ SET**      | **MF \_ E \_ TRANSFORM \_ TYPE \_ NOT \_ SET** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Criando objetos DMO/MFT híbridos

A interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) é baseada livremente em [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)que é a interface principal para DMOs (Objetos de Mídia DirectX). É possível criar objetos que expõem ambas as interfaces. No entanto, isso pode levar a colisões de nomeação, pois as interfaces têm alguns métodos que compartilham o mesmo nome. Você pode resolver esse problema de uma das duas maneiras:

Solução 1: inclua a seguinte linha na parte superior de qualquer arquivo .cpp que contenha funções MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Isso altera a declaração da interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) para que a maioria dos nomes de método seja prefixada com "MFT". Assim, [**IMFTransform::P rocessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) **torna-se IMFTransform::MFTProcessInput**, enquanto [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) mantém seu nome original. Essa técnica será mais útil se você estiver convertendo um DMO existente em um DMO/MFT híbrido. Você pode adicionar os novos métodos MFT sem alterar os métodos DMO dados.

Solução 2: use a sintaxe C++ para desambiguar nomes herdados de mais de uma interface. Por exemplo, declare a versão MFT [**do ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) da seguinte forma:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Declare a DMO do [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) da mesma forma:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Se você fizer uma chamada interna para um método dentro do objeto , poderá usar essa sintaxe, mas fazer isso substituirá o status virtual do método. Uma maneira melhor de fazer chamadas de dentro do objeto é a seguinte:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Dessa forma, se você derivar outra classe de **CMyHybridObject** e substituir o método CMyHybridObject::IMediaObject::P rocessInput, o método virtual correto será chamado. As interfaces DMO são documentadas na documentação DirectShow SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 
