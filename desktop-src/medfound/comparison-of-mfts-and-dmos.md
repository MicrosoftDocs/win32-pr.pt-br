---
description: As transformações de Media Foundation (MFTs) são uma evolução do modelo de transformação introduzido pela primeira vez com o DirectX Media Objects (DMOs).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Comparação de MFTs e DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010321"
---
# <a name="comparison-of-mfts-and-dmos"></a>Comparação de MFTs e DMOs

As transformações de Media Foundation (MFTs) são uma evolução do modelo de transformação introduzido pela primeira vez com o DirectX Media Objects (DMOs). Este tópico resume as principais maneiras pelas quais o MFTs difere do DMOs. Leia este tópico se você já estiver familiarizado com as interfaces DMO ou se quiser converter um DMO existente em um MFT.

Este tópico contém as seguintes seções:

-   [Número de fluxos](#number-of-streams)
-   [Negociação de formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Alocando recursos](#allocating-resources)
    -   [Processando dados](#processing-data)
    -   [Liberação](#flushing)
    -   [Descontinuidades de fluxo](#stream-discontinuities)
-   [Diferenças diversas](#miscellaneous-differences)
-   [Sinalizadores](#flags)
    -   [Sinalizadores de ProcessInput](#processinput-flags)
    -   [Sinalizadores de ProcessOutput](#processoutput-flags)
    -   [Sinalizadores de GetInputStatus](#getinputstatus-flags)
    -   [Sinalizadores de GetOutputStatus](#getoutputstatus-flags)
    -   [Sinalizadores de GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Sinalizadores de GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Sinalizadores SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Códigos de Erro](#error-codes)
-   [Criando objetos DMO/MFT híbridos](#creating-hybrid-dmomft-objects)
-   [Tópicos relacionados](#related-topics)

## <a name="number-of-streams"></a>Número de fluxos

Um DMO tem um número fixo de fluxos, enquanto um MFT pode dar suporte a um número dinâmico de fluxos. O cliente pode adicionar fluxos de entrada e o MFT pode adicionar novos fluxos de saída durante o processamento. No entanto, o MFTs não é necessário para dar suporte a fluxos dinâmicos. Uma MFT pode ter um número fixo de fluxos, assim como um DMO.

Os métodos a seguir são usados para dar suporte a fluxos dinâmicos em um MFT:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Além disso, o método [**IMFTransform::P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) define o comportamento para adicionar ou remover fluxos de saída.

Como DMOs têm fluxos fixos, os fluxos em um DMO são identificados usando valores de índice com base em zero. MFTs, por outro lado, usar identificadores de fluxo que não correspondem necessariamente aos valores de índice. Isso ocorre porque o número de fluxos em um MFT pode ser alterado. Por exemplo, o fluxo 0 pode ser removido, deixando o fluxo 1 como o primeiro fluxo. No entanto, um MFT com um número fixo de fluxos deve observar a mesma convenção que DMOs e usar valores de índice para identificadores de fluxo.

## <a name="format-negotiation"></a>Negociação de formato

MFTs use a interface [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) para descrever os tipos de mídia. Caso contrário, a negociação de formato com MFTs funcionará nos mesmos princípios básicos que com o DMOs. A tabela a seguir lista os métodos de negociação de formato para DMOs e os métodos correspondentes para MFTs.



| Método DMO                                                                        | Método MFT                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Como DMOs, MFTs processa dados por meio de chamadas para os métodos [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Aqui estão as principais diferenças entre os processos DMO e MFT ao transmitir dados.

### <a name="allocating-resources"></a>Alocando recursos

MFTs não tem os métodos [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) e [**IMediaObject:: FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) usados com DMOs. Para lidar com a alocação e a desalocação de recursos com eficiência, um MFT pode responder às seguintes mensagens no método [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**notificação de mensagem de MFT \_ \_ \_ Iniciar \_ streaming**](mft-message-notify-begin-streaming.md)
-   [**\_ \_ \_ início \_ da notificação de \_ mensagem MFT**](mft-message-notify-start-of-stream.md)

Além disso, o cliente pode sinalizar o início e o término de um fluxo chamando [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com as seguintes mensagens:

-   [**\_ \_ \_ fim \_ da notificação de \_ mensagem MFT**](mft-message-notify-end-of-stream.md)
-   [**\_fim da \_ notificação de mensagem \_ de MFT \_**](mft-message-notify-end-streaming.md)

Essas duas mensagens não têm nenhum equivalente de DMO exato.

### <a name="processing-data"></a>Processando dados

MFTs Use amostras de mídia para manter os dados de entrada e saída. Os exemplos de mídia expõem a interface [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) e contêm os seguintes dados:

-   Carimbo de data/hora e duração.
-   Atributos que contêm informações por exemplo. Para obter uma lista de atributos, consulte [atributos de exemplo](sample-attributes.md).
-   Zero ou mais buffers de mídia. Cada buffer de mídia expõe a interface [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

A interface [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) é semelhante à interface DMO **IMediaBuffer** . Para acessar o buffer de memória subjacente, chame [**IMFMediaBuffer:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Esse método é aproximadamente equivalente a [**IMediaBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) para DMOs.

Para dados de vídeo não compactados, um buffer de mídia também pode dar suporte à interface [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Um MFT que processa vídeo descompactado (como entrada ou saída) deve estar preparado para usar a interface **IMF2DBuffer** se o buffer o expuser. Para obter mais informações, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).

Media Foundation fornece algumas implementações padrão de [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), portanto, geralmente não é necessário escrever sua própria implementação. Para criar um buffer de DMO a partir de um buffer de Media Foundation, chame [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Liberação

MFTs não tem um método [**flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Para liberar uma MFT, chame [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de [**\_ liberação de \_ comando \_ da mensagem MFT**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Descontinuidades de fluxo

MFTs não tem um método de [**descontinuidade**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Para sinalizar uma descontinuidade em um fluxo, defina o atributo de [**\_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no exemplo de entrada.

## <a name="miscellaneous-differences"></a>Diferenças diversas

Aqui estão algumas diferenças secundárias adicionais entre MFTs e DMOs.

-   Não há equivalentes de MFT para os seguintes métodos de DMO:
    -   [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   MFTs não são necessários para dar suporte à agregação.
-   MFTs dá suporte a uma operação chamada *drenagem*. A finalidade do descarregamento é processar todos os dados que permanecem no MF, sem fornecer mais dados de entrada para o MFT (por exemplo, no final do fluxo). Para drenar uma MFT, chame [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de [**dreno de \_ \_ comando \_ de mensagem MFT**](mft-message-command-drain.md) . Para obter mais informações, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).
-   MFTs pode ter atributos, incluindo atributos por fluxo. Use os métodos a seguir para obter os atributos de um MFT:

    -   [**IMFTransform:: GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs pode processar eventos. Para enviar um evento para um MFT, chame [**IMFTransform::P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Uma MFT pode enviar um evento para o cliente por meio do método [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Para obter mais informações, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).

## <a name="flags"></a>Flags

As tabelas a seguir listam os vários sinalizadores de DMO e seus equivalentes de MFT. Sempre que um sinalizador de DMO é mapeado diretamente para um sinalizador de MFT, ambos os sinalizadores têm o mesmo valor numérico. No entanto, alguns sinalizadores de DMO não têm equivalentes de MFT exatos e vice-versa.

### <a name="processinput-flags"></a>Sinalizadores de ProcessInput

DMOs: a enumeração de [**\_ \_ sinalizadores do buffer de dados de entrada \_ \_ \_ do DMO**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) .

MFTs: nenhuma Enumeração equivalente.



| Sinalizador de DMO                                  | Sinalizador de MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **dados de entrada de DMO \_ \_ \_ BUFFERF \_ ponto**  | Nenhum sinalizador equivalente. Em vez disso, defina o atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo. |
| **\_tempo de \_ BUFFERF de dados de entrada de DMO \_ \_**       | Nenhum sinalizador equivalente. Em vez disso, chame [**IMFSample:: Setamostratime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) no exemplo.                                  |
| **\_tempo de \_ BUFFERF de dados de entrada de DMO \_ \_** | Nenhum sinalizador equivalente. Em vez disso, chame [**IMFSample:: SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) no exemplo.                          |



 

### <a name="processoutput-flags"></a>Sinalizadores de ProcessOutput

DMOs: a enumeração de [**\_ \_ sinalizadores de \_ saída \_ do processo DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) .

MFTs: enumeração de [**\_ \_ sinalizadores de \_ saída \_ do processo de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| Sinalizador de DMO                                            | Sinalizador de MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_descarte de saída do processo DMO \_ \_ \_ quando \_ não houver \_ buffer** | **Descarte de saída de processo de MFT \_ \_ \_ \_ quando \_ nenhum \_ buffer** |



 

Enumeração de [**\_ \_ sinalizadores de \_ \_ buffer de \_ dados de saída**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) DMOs: DMO.


MFTs: enumeração de [**\_ \_ sinalizadores do buffer de dados de saída \_ \_ \_ da MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| Sinalizador de DMO                                   | Sinalizador de MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **dados de saída de DMO \_ \_ \_ BUFFERF \_ ponto**  | Nenhum sinalizador equivalente. Em vez disso, verifique o atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo. |
| **\_tempo de \_ BUFFERF de dados de saída de DMO \_ \_**       | Nenhum sinalizador equivalente. Em vez disso, chame [**IMFSample:: Getsampletime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) no exemplo.                                        |
| **\_tempo de \_ BUFFERF de dados de saída de DMO \_ \_** | Nenhum sinalizador equivalente. Em vez disso, chame [**IMFSample:: GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) no exemplo.                                |
| **BUFFERF de dados de saída de DMO \_ \_ \_ \_ incompleto** | **BUFFER de dados de saída de MFT \_ \_ \_ \_ incompleto**                                                                                                           |
| Nenhum sinalizador equivalente.                        | **\_alteração do \_ formato do buffer de dados de saída da \_ \_ MFT \_**                                                                                                       |
| Nenhum sinalizador equivalente.                        | **\_fim do \_ fluxo do buffer de dados de saída da \_ \_ MFT \_**                                                                                                          |
| Nenhum sinalizador equivalente.                        | **BUFFER de dados de saída de MFT \_ \_ \_ \_ sem \_ amostra**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Sinalizadores de GetInputStatus

DMOs: a enumeração de **\_ \_ sinalizadores de \_ status \_ de entrada de DMO** .

MFTs: enumeração de [**\_ \_ sinalizadores de \_ status \_ de entrada da MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| Sinalizador de DMO                              | Sinalizador de MFT                             |
|---------------------------------------|--------------------------------------|
| **STATUSF de entrada de DMO- \_ \_ \_ aceitar \_ dados** | **\_dados de \_ aceitação do status de entrada de MFT \_ \_** |



 

### <a name="getoutputstatus-flags"></a>Sinalizadores de GetOutputStatus

DMOs: nenhuma Enumeração equivalente.

MFTs: enumeração de [**\_ \_ sinalizadores de \_ status \_ de saída de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| Sinalizador de DMO            | Sinalizador de MFT                               |
|---------------------|----------------------------------------|
| Nenhum sinalizador equivalente. | **exemplo de status de saída de MFT \_ \_ \_ \_ pronto** |



 

### <a name="getinputstreaminfo-flags"></a>Sinalizadores de GetInputStreamInfo

DMOs: DMO enumeração de [**\_ \_ sinalizadores de informações de \_ fluxo \_ \_ de entrada**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) .

MFTs: enumeração de [**\_ \_ sinalizadores de informações de fluxo de entrada \_ \_ \_ de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) .



| Sinalizador de DMO                                             | Sinalizador de MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_ \_ \_ exemplos completos de entrada do DMO STREAMF \_**              | **\_ \_ amostras completas do fluxo de entrada de \_ MFT \_**              |
| **STREAMF de entrada de DMO de \_ \_ \_ \_ amostra única \_ por \_ buffer** | **\_amostra única de fluxo de entrada de MFT \_ \_ \_ \_ por \_ buffer** |
| **\_tamanho de \_ \_ amostra fixo \_ STREAMF \_ de entrada DMO**         | **\_tamanho de \_ \_ amostra fixo \_ do fluxo de entrada da \_ MFT**         |
| **entrada de DMO \_ \_ STREAMF \_ armazena \_ buffers**              | **fluxo de entrada de MFT \_ \_ \_ armazena \_ buffers**              |
| Nenhum sinalizador equivalente.                                  | **o fluxo de entrada de MFT não \_ \_ \_ é \_ \_ ADDREF**           |
| Nenhum sinalizador equivalente.                                  | **fluxo de entrada do MFT \_ \_ \_ removível**                   |
| Nenhum sinalizador equivalente.                                  | **fluxo de entrada de MFT \_ \_ \_ opcional**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Sinalizadores de GetOutputStreamInfo

DMOs: DMO enumeração de [**\_ \_ sinalizadores de informações de \_ fluxo \_ \_ de saída**](/previous-versions/ms806053(v=msdn.10)) .

MFTs: enumeração de [**\_ \_ sinalizadores de informações do fluxo de saída \_ \_ \_ da MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) .



| Sinalizador de DMO                                              | Sinalizador de MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_ \_ amostras completas de STREAMF de saída de \_ DMO \_**              | **\_ \_ amostras completas do fluxo de saída da \_ MFT \_**              |
| **STREAMF de saída de DMO de \_ \_ \_ \_ exemplo único \_ por \_ buffer** | **\_amostra única de fluxo de saída de MFT \_ \_ \_ \_ por \_ buffer** |
| **\_tamanho de \_ \_ amostra fixo \_ STREAMF \_ de saída DMO**         | **\_tamanho da \_ \_ amostra fixa \_ do fluxo de saída da \_ MFT**         |
| **STREAMF de saída de DMO \_ \_ \_ Descartado**                 | **fluxo de saída de MFT \_ \_ \_ Descartado**                 |
| **STREAMF de saída de DMO \_ \_ \_ opcional**                    | **fluxo de saída de MFT \_ \_ \_ opcional**                    |
| Nenhum sinalizador equivalente.                                   | **o \_ fluxo de saída de MFT \_ \_ fornece \_ exemplos**           |
| Nenhum sinalizador equivalente.                                   | **o \_ fluxo de saída de MFT \_ \_ pode \_ fornecer \_ exemplos**       |
| Nenhum sinalizador equivalente.                                   | **\_ \_ leitura lenta do fluxo de saída da \_ MFT \_**                  |
| Nenhum sinalizador equivalente.                                   | **fluxo de saída do MFT \_ \_ \_ removível**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Sinalizadores SetInputType/SetOutputType

DMOs: [**\_ DMO \_ definir \_ \_**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) enumeração de sinalizadores de tipo.

MFTs: enumeração de [**\_ \_ sinalizadores de \_ tipo \_ de conjunto de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| Sinalizador de DMO                        | Sinalizador de MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO \_ set \_ TYPEF \_ \_ somente teste** | **\_ \_ somente teste de tipo de conjunto de \_ MFT \_**                                                       |
| **DMO \_ set \_ TYPEF \_ Clear**      | Nenhum sinalizador equivalente. Em vez disso, defina o tipo de mídia como **nulo** para limpar o tipo de mídia. |



 

## <a name="error-codes"></a>Códigos de erro

A tabela a seguir mostra como mapear códigos de erro de DMO para códigos de erro de MFT. Um objeto MFT/DMO híbrido deve retornar os códigos de erro DMO dos métodos [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e os códigos de erro MFT dos métodos [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . Os códigos de erro do DMO são definidos no arquivo de cabeçalho MediaErr. h. Os códigos de erro de MFT são definidos no arquivo de cabeçalho mferror. h.



| Código de erro DMO                  | Código de erro MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ inválidotype**         | **MF \_ E \_ invalidatype**               |
| **DMO \_ E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **DMO \_ E não \_ aceitar**        | **MF \_ E não \_ aceitar**              |
| **DMO \_ E \_ não há \_ mais \_ itens**     | **MF \_ E \_ não há \_ mais \_ tipos**           |
| **\_E \_ tipo DMO \_ não \_ aceito** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_E tipo de DMO \_ \_ não \_ definido**      | **\_tipo de transformação MF E \_ \_ \_ não \_ definido** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Criando objetos DMO/MFT híbridos

A interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) é livremente baseada em [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), que é a interface principal para DMOs (DirectX Media Objects). É possível criar objetos que expõem ambas as interfaces. No entanto, isso pode levar à nomenclatura de colisões, porque as interfaces têm alguns métodos que compartilham o mesmo nome. Você pode resolver esse problema de uma das duas maneiras:

Solução 1: inclua a linha a seguir na parte superior de qualquer arquivo. cpp que contenha funções de MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Isso altera a declaração da interface [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) para que a maioria dos nomes de método seja prefixada com "MFT". Portanto, [**IMFTransform::P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) se torna **IMFTransform:: MFTProcessInput**, enquanto [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) mantém seu nome original. Essa técnica será mais útil se você estiver convertendo um DMO existente em um DMO/MFT híbrido. Você pode adicionar os novos métodos de MFT sem alterar os métodos de DMO.

Solução 2: Use a sintaxe C++ para desambiguar nomes que são herdados de mais de uma interface. Por exemplo, declare a versão de MFT do [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) da seguinte maneira:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Declare a versão DMO do [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) da seguinte maneira:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Se você fizer uma chamada interna para um método dentro do objeto, poderá usar essa sintaxe, mas isso substituirá o status virtual do método. Uma maneira melhor de fazer chamadas de dentro do objeto é a seguinte:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Dessa forma, se você derivar outra classe de **CMyHybridObject** e substituir o método CMyHybridObject:: IMediaObject::P rocessinput, o método virtual correto será chamado. As interfaces DMO estão documentadas na documentação do SDK do DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
