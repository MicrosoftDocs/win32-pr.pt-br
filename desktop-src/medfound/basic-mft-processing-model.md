---
description: Este tópico descreve como um cliente usa uma Media Foundation transformação (MFT) para processar dados. O cliente é qualquer coisa que chama diretamente os métodos no MFT. Esse pode ser o aplicativo ou o pipeline de Media Foundation.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modelo de processamento de MFT básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a1edb0c5144c6e3a3e1825e637cd5d19049699ad60bbf764629c9ade7cd3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035444"
---
# <a name="basic-mft-processing-model"></a>Modelo de processamento de MFT básico

Este tópico descreve como um cliente usa uma Media Foundation transformação (MFT) para processar dados. O *cliente* é qualquer coisa que chama diretamente os métodos no MFT. Esse pode ser o aplicativo ou o pipeline de Media Foundation.

Leia este tópico se você estiver:

-   Gravar um aplicativo que faz chamadas diretas para um ou mais MFTs.
-   Gravar uma MFT personalizada e desejar entender o comportamento esperado de um MFT.

Este tópico descreve um modelo de processamento *síncrono* . Nesse modelo, todos os métodos de processamento de dados são bloqueados até que sejam concluídos. O MFTs também pode oferecer suporte a um modelo *assíncrono* , que é descrito no tópico [MFTs assíncrona](asynchronous-mfts.md).

-   [Modelo de processamento básico](#basic-processing-model)
    -   [Criar o MFT](#create-the-mft)
    -   [Obter identificadores de fluxo](#get-stream-identifiers)
    -   [Definir tipos de mídia](#set-media-types)
    -   [Obter requisitos de buffer](#get-buffer-requirements)
    -   [Processar dados](#process-data)
-   [Extensões para o modelo básico](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Liberando uma MFT](#flushing-an-mft)
-   [Drenagem de um MFT](#draining-an-mft)
-   [Atributos de exemplo](#sample-attributes)
-   [Descontinuidades](#discontinuities)
-   [Alterações de formato dinâmico](#dynamic-format-changes)
-   [Eventos de fluxo](#stream-events)
-   [Tópicos relacionados](#related-topics)

## <a name="basic-processing-model"></a>Modelo de processamento básico

### <a name="create-the-mft"></a>Criar o MFT

Há várias maneiras de criar um MFT:

-   Chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .
-   Chame a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Se você já souber o CLSID do MFT, basta chamar **CoCreateInstance**.

Alguns MFTs podem fornecer outras opções, como uma função de criação especializada.

### <a name="get-stream-identifiers"></a>Obter identificadores de fluxo

Uma MFT tem um ou mais *fluxos*. Os fluxos de entrada recebem dados de entrada e os fluxos de saída geram dados de saída. os Fluxos não são representados como objetos distintos. Em vez disso, vários métodos de MFT usam identificadores de fluxo como parâmetros.

Alguns MFTs permitem que o cliente adicione ou remova fluxos de entrada. Durante o streaming, um MFT pode adicionar ou remover fluxos de saída. (O cliente não pode adicionar ou remover fluxos de saída.)

1.  (Opcional.) Chame [**IMFTransform:: GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) para obter o número mínimo e máximo de fluxos para os quais o MFT pode dar suporte. Se o mínimo e o máximo forem os mesmos, o MFT terá um número fixo de fluxos.
2.  Chame [**IMFTransform:: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) para obter o número inicial de fluxos.
3.  Chame [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) para obter os identificadores de fluxo. Se esse método retornar E \_ NOTIMPL, isso significará que o MFT tem um número fixo de fluxos e que os identificadores de fluxo são consecutivos a partir de zero.
4.  (Opcional.) Se a MFT não tiver um número fixo de fluxos, chame [**IMFTransform:: AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) para adicionar mais fluxos de entrada ou [**IMFTransform::D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) para remover os fluxos de entrada. (Você não pode adicionar ou remover fluxos de saída.)

### <a name="set-media-types"></a>Definir tipos de mídia

Antes que um MFT possa processar dados, o cliente deve definir um tipo de mídia para cada um dos fluxos do MFT. Um MFT pode exigir que o cliente defina os tipos de entrada antes de definir os tipos de saída ou que possam exigir a ordem oposta (os tipos de saída primeiro). Alguns MFTs não têm um requisito no pedido.

Uma MFT pode fornecer uma lista de tipos de mídia preferenciais para um fluxo. Além disso, o MFTs pode indicar os formatos gerais aos quais eles dão suporte adicionando essas informações ao registro.

Para definir os tipos de mídia, faça o seguinte:

1.  (Opcional.) Para cada fluxo de entrada, chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obter a lista de tipos preferenciais para esse fluxo.
    -   Se esse método retornar \_ \_ \_ o tipo de impressão MF e Transform \_ não \_ definido, você deverá primeiro definir os tipos de saída; pule para a etapa 3.
    -   Se o método retornar E \_ NOTIMPL, o MFT não terá uma lista de tipos de entrada preferenciais; pule para a etapa 2.
2.  Para cada fluxo de entrada, chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de entrada. Você pode usar um tipo de mídia da etapa 1 ou um tipo que descreva os dados de entrada. Se qualquer fluxo retornar o \_ tipo de MF E de \_ transformação \_ \_ não \_ definido, pule para a etapa 3.
3.  (Opcional.) Para cada fluxo de saída, chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter uma lista de tipos preferenciais para esse fluxo.
    -   Se esse método retornar \_ \_ \_ o tipo de saída MF e Transform \_ não \_ definido, você deverá definir os tipos de entrada primeiro; volte para a etapa 1.
    -   Se qualquer fluxo retornar E \_ NOTIMPL, o MFT não terá uma lista de tipos de saída preferenciais; pule para a etapa 4.
4.  Para cada fluxo de saída, chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de saída. Você pode usar um tipo de mídia da etapa 3 ou um tipo que descreva o formato de saída necessário.
5.  Se qualquer fluxo de entrada não tiver um tipo de mídia, volte para a etapa 1.

### <a name="get-buffer-requirements"></a>Obter requisitos de buffer

Depois que o cliente define os tipos de mídia, ele deve obter os requisitos de buffer para cada fluxo:

-   Para cada fluxo de entrada, chame [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Para cada fluxo de saída, chame [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Processar Dados

Uma MFT foi projetada para ser uma máquina de estado confiável. Ele não faz nenhuma chamada de volta para o cliente.

1.  Chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a [**\_ mensagem MFT \_ notificar \_ Iniciar \_**](mft-message-notify-begin-streaming.md) mensagem de streaming. Essa mensagem solicita que o MFT aloque os recursos necessários durante o streaming.
2.  Chame [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) em pelo menos um fluxo de entrada para entregar um exemplo de entrada para o MFT.
3.  (Opcional.) Chame [**IMFTransform:: GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) para consultar se o MFT pode gerar um exemplo de saída. Se o método retornar S \_ OK, verifique o parâmetro *pdwFlags* . Se *pdwFlags* contiver o sinalizador **\_ \_ \_ \_ pronto de exemplo status de saída do MFT** , vá para a etapa 4. Se *pdwFlags* for zero, volte para a etapa 2. Se o método retornar E \_ NOTIMPL, vá para a etapa 4.
4.  Chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter dados de saída.
    -   Se o método retornar **MF \_ E a \_ transformação \_ precisar de \_ mais \_ entradas**, isso significará que o MFT requer mais dados de entrada; volte para a etapa 2.
    -   Se o método retornar **a \_ \_ alteração de \_ fluxo \_ de MF e de transformação**, isso significará que o número de fluxos de saída foi alterado ou o formato de saída foi alterado. O cliente pode precisar consultar novos identificadores de fluxo ou definir novos tipos de mídia. Para obter mais informações, consulte a documentação de [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Se ainda houver dados de entrada para processar, vá para a etapa 2. Se o MFT tiver consumido todos os dados de entrada disponíveis, vá para a etapa 6.
6.  Chame [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a [**mensagem de MFT \_ \_ notificar \_ fim \_ da mensagem de \_ fluxo**](mft-message-notify-end-of-stream.md) .
7.  Chame [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de [**\_ dreno de \_ comando \_ de mensagem MFT**](mft-message-command-drain.md) .
8.  Chame [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter a saída restante. Repita essa etapa até que o método retorne **MF \_ E a \_ transformação \_ precise de \_ mais \_ entradas**. Esse valor de retorno sinaliza que toda a saída foi descarregada da MFT. (Não trate isso como uma condição de erro.)

A sequência descrita aqui mantém o mínimo possível de dados na MFT. Depois de cada chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), o cliente tenta obter a saída. Várias amostras de entrada podem ser necessárias para produzir um exemplo de saída ou um único exemplo de entrada pode gerar várias amostras de saída. O comportamento ideal para o cliente é efetuar pull de amostras de saída do MFT até que a MFT exija mais entrada.

No entanto, o MFT deve ser capaz de lidar com uma ordem diferente de chamadas de método pelo cliente. Por exemplo, o cliente pode simplesmente alternar entre chamadas para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). O MFT deve restringir a quantidade de entrada obtida retornando **MF E não \_ \_ aceitando** de **ProcessInput** sempre que tiver alguma saída a ser produzida.

A ordem das chamadas de método descritas aqui não é a única sequência válida de eventos. Por exemplo, as etapas 3 e 4 pressupõem que o cliente comece com os tipos de entrada e, em seguida, tente os tipos de saída. O cliente também pode reverter essa ordem e começar com os tipos de saída. Em ambos os casos, se o MFT exigir a ordem oposta, ele deverá retornar o código de erro MF \_ E o \_ tipo de transformação \_ \_ não \_ definido.

O cliente pode chamar métodos informativos, como [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) e [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo), a qualquer momento durante o streaming. O cliente também pode tentar alterar os tipos de mídia a qualquer momento. O MFT deve retornar um código de erro se essa não for uma operação válida. Em suma, MFTs deve assumir muito pouco a ordem das operações, além da que está documentada nas próprias chamadas.

O diagrama a seguir mostra um gráfico de fluxo dos procedimentos descritos neste tópico.

![fluxograma que leva de identificadores de fluxo Get por meio de loops que definem tipos de entrada, recebem entrada e saída de processo](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Extensões para o modelo básico

Opcionalmente, uma MFT pode dar suporte a algumas extensões para o modelo de streaming básico.

-   Fluxos de leitura lenta. Se o método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retornar o sinalizador de **\_ \_ \_ \_ leitura lenta do fluxo de saída do MFT** para um fluxo de saída, o cliente não precisará coletar dados desse fluxo de saída. O MFT continua aceitando a entrada e, em algum momento, o MFT descartará os dados de saída desse fluxo. Se todos os fluxos de saída tiverem esse sinalizador, o MFT nunca falhará ao aceitar a entrada. Um exemplo pode ser uma transformação de visualização, em que o cliente obtém a saída somente quando tem ciclos de CPU sobressalentes para desenhar a visualização.
-   Fluxos descartados. Se o método [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retornar o **sinalizador \_ \_ \_ descartado do fluxo de saída do MFT** para um fluxo de saída, o cliente poderá solicitar que o MFT descarte a saída, mas o MFT não descartará nenhuma saída, a menos que solicitado. Quando o MFT atinge seu buffer de entrada máximo, o cliente deve coletar alguns dados de saída ou solicitar o MFT para descartar a saída.
-   Fluxos opcionais. Se o método [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retornar o **sinalizador \_ \_ \_ opcional do fluxo de saída do MFT** para um fluxo de saída ou o método [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) retornar o sinalizador **\_ \_ \_ opcional do fluxo de entrada do MFT** para um fluxo de entrada, esse fluxo será opcional. O cliente não precisa definir um tipo de mídia no fluxo. Se o cliente não definir o tipo, o fluxo será desmarcado. Um fluxo de saída desmarcado não produz amostras e o cliente não fornece um buffer para o fluxo quando chama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Um fluxo de entrada desmarcado não aceita dados de entrada. Um MFT pode marcar todos os seus fluxos de entrada e saída como opcionais. No entanto, espera-se que pelo menos uma entrada e uma saída devam ser selecionadas para que o MFT funcione.
-   Processamento assíncrono. o modelo de processamento assíncrono foi introduzido no Windows 7. Ele é descrito no tópico [MFTs assíncrona](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

Se um MFT processar dados de vídeo descompactados, ele deverá usar a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) para manipular os buffers de exemplo. Para obter essa interface, consulte a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) em qualquer buffer de entrada ou saída. Não usar essa interface quando ela estiver disponível pode resultar em cópias de buffer adicionais. Para fazer uso adequado dessa interface, a transformação não deve bloquear o buffer usando a interface **IMFMediaBuffer** quando **IMF2DBuffer** está disponível.

Para obter mais informações sobre o processamento de dados de vídeo, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Liberando uma MFT

A *liberação* de um MFT faz com que o MFT descarte todos os seus dados de entrada. Isso pode causar uma interrupção no fluxo de saída. Um cliente normalmente liberaria um MFT antes de buscar um novo ponto no fluxo de entrada ou alternando para um novo fluxo de entrada, quando o cliente não se preocupa com a perda de dados.

Para liberar uma MFT, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de [**\_ liberação de \_ comando \_ da mensagem MFT**](mft-message-command-flush.md) .

## <a name="draining-an-mft"></a>Drenagem de um MFT

O *descarregamento* de uma MFT faz com que o MFT produza o máximo de saída possível de qualquer dado de entrada já enviado. Se o MFT não puder produzir um exemplo de saída completa da entrada disponível, ele removerá os dados de entrada. Um cliente normalmente drenaria um MFT quando atingiu o final do fluxo de origem, ou imediatamente antes de uma alteração de formato no fluxo de origem. Para drenar uma MFT, faça o seguinte:

1.  Chame [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de [**\_ dreno de \_ comando \_ de mensagem MFT**](mft-message-command-drain.md) . Essa mensagem notifica o MFT de que ele deve fornecer tantos dados de saída quanto puder dos dados de entrada que já foram enviados.
2.  Chame [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter dados de saída, até que o método retorne **MF \_ E \_ Transform \_ precise de \_ mais \_ entradas**.

Enquanto a MFT está sendo descarregada, ela não aceitará mais nenhuma entrada.

## <a name="sample-attributes"></a>Atributos de exemplo

Os exemplos de entrada podem ter atributos que devem ser copiados para os exemplos de saída correspondentes.

-   Se o MFT retornar a **variante \_ true** para a propriedade [**\_ \_ com suporte do exattribute MFPKEY**](mfpkey-exattribute-supported-property.md) , o MFT deverá copiar os atributos.
-   Se a [**propriedade \_ \_ com suporte do exattribute MFPKEY**](mfpkey-exattribute-supported-property.md) for **Variant \_ false** ou não estiver definida, o cliente deverá copiar os atributos.

Para um MFT com uma entrada e uma saída, você pode usar a seguinte regra geral:

-   Se cada amostra de entrada produzir exatamente um exemplo de saída, você poderá permitir que o cliente Copie os atributos. Deixe a [**propriedade \_ \_ com suporte FileAttribute MFPKEY**](mfpkey-exattribute-supported-property.md) .
-   Se não houver uma correspondência um-para-um entre amostras de entrada e amostras de saída, o MFT deverá determinar os atributos corretos para exemplos de saída. Defina a [**propriedade \_ \_ com suporte do FileAttribute MFPKEY**](mfpkey-exattribute-supported-property.md) como **Variant \_ true**.

## <a name="discontinuities"></a>Descontinuidades

Uma descontinuidade é uma interrupção em um fluxo de áudio ou vídeo. Descontinuidades pode ser causado por pacotes descartados em uma conexão de rede, dados de arquivo corrompidos, uma mudança de um fluxo de origem para outro ou uma ampla gama de outras causas. Descontinuidades são sinalizados definindo o atributo [**de \_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no primeiro exemplo após a descontinuidade. Não é possível sinalizar uma descontinuidade no meio de um exemplo. Portanto, todos os dados descontínuos devem ser enviados em amostras separadas.

Algumas transformações, especialmente aquelas que lidam com dados não compactados, como efeitos de áudio e vídeo, devem ignorar descontinuidades quando processam dados de entrada. Esses MFTs geralmente são projetados para lidar com dados contínuos e devem tratar todos os dados que receberem como contínuos, mesmo após uma descontinuidade.

Se uma MFT ignorar uma descontinuidade nos dados de entrada, ela ainda deverá definir o sinalizador de discontinuidade no exemplo de saída, se o exemplo de saída tiver o mesmo carimbo de data/hora que o exemplo de entrada. No entanto, se o exemplo de saída tiver um carimbo de data/hora diferente, o MFT não deverá propagar a descontinuidade. (Esse seria o caso em alguns reamostradores de áudio, por exemplo.) Uma descontinuidade no local errado no fluxo é pior do que nenhuma descontinuidade.

A maioria dos decodificadores não pode ignorar descontinuidades, porque uma descontinuidade afeta a interpretação da próxima amostra. Qualquer tecnologia de codificação que usa compactação entre quadros, como MPEG-2, se encaixa nessa categoria. Alguns esquemas de codificação usam apenas a compactação intra-frame, como DV e MJPEG. Esses decodificadores podem ignorar descontinuidades com segurança.

As transformações que respondem a descontinuidades devem geralmente produzir a mesma quantidade de dados antes da descontinuidade como podem e descartar o restante. O exemplo de entrada com o sinalizador de descontinuidade deve ser processado como se fosse o primeiro exemplo no fluxo. (Esse comportamento corresponde ao que é especificado para a mensagem de [**\_ dreno de \_ comando \_ de mensagem MFT**](mft-message-command-drain.md) .) No entanto, os detalhes exatos dependerão do formato de mídia.

Se um decodificador não faz nada para mitigar uma descontinuidade, ele deve copiar o sinalizador de descontinuidade para os dados de saída. Demultiplexadores e outros MFTs que funcionam inteiramente com dados compactados devem copiar qualquer descontinuidades para seus fluxos de saída. Caso contrário, os componentes downstream talvez não consigam decodificar os dados compactados corretamente. Em geral, é quase sempre correto para passar descontinuidades downstream, a menos que o MFT contenha um código explícito para suavizar o descontinuidades.

## <a name="dynamic-format-changes"></a>Alterações de formato dinâmico

Os formatos podem ser alterados durante o streaming. Por exemplo, a taxa de proporção pode ser alterada no meio de um fluxo de vídeo.

Para obter detalhes sobre como as alterações de fluxo são tratadas por um MFT, consulte [manipulando alterações de fluxo](handling-stream-changes.md).

## <a name="stream-events"></a>Eventos de fluxo

Para enviar um evento para um MFT, chame [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Se o método retornar **o \_ evento MF S \_ Transform \_ \_ não \_ propagar \_**, o MFT retornará o evento para o chamador em uma chamada subsequente para [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se o método retornar qualquer outro valor **HRESULT** , o MFT não retornará o evento para o cliente em **ProcessOutput**. Nesse caso, o cliente é responsável por propagar o downstream de evento para o próximo componente no pipeline, se aplicável. Para obter mais informações, consulte [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



