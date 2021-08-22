---
description: Este tópico descreve como implementar uma fonte de mídia personalizada no Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Escrevendo uma fonte de mídia personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e240277d5bbbabe5068f3a5f10bdb0312c29410def51bdced14715c1d3d68b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343186"
---
# <a name="writing-a-custom-media-source"></a>Escrevendo uma fonte de mídia personalizada

Este tópico descreve como implementar uma fonte de mídia personalizada no Microsoft Media Foundation. Ele contém as seções a seguir:

-   [Criando o descritor de apresentação](#creating-the-presentation-descriptor)
-   [Iniciando a fonte de mídia](#starting-the-media-source)
    -   [Procurando](#seeking)
-   [Pausando a fonte de mídia](#pausing-the-media-source)
-   [Gerando dados de origem](#generating-source-data)
    -   [Solicitações de exemplo](#sample-requests)
    -   [Alocando exemplos](#allocating-samples)
    -   [Lacunas no fluxo](#gaps-in-the-stream)
-   [Desligando a fonte de mídia](#shutting-down-the-media-source)
-   [Fontes ao vivo](#live-sources)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Criando o descritor de apresentação

O [**método IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) retorna uma cópia do descritor de apresentação da origem. Para criar o descritor de apresentação, você deve saber o número de fluxos no conteúdo de origem e os possíveis formatos de cada fluxo. Para cada fluxo, crie um descritor de fluxo da seguinte forma:

1.  Crie uma matriz de tipos de mídia. Cada tipo de mídia na matriz representa um formato possível para o fluxo. Para obter mais informações sobre como criar tipos de mídia, consulte [Tipos de mídia](media-types.md).
2.  Chame [**MFCreateStreamDescriptor para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) criar o descritor de fluxo. Passe a matriz de tipos de mídia. A função retorna um [**ponteiro IMFStreamDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
3.  Chame [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obter o manipulador de tipo de mídia do descritor de fluxo.
4.  Chame [**IMFMediaTypeHandler::SetCurrentMediaType para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) definir o formato de fluxo padrão. Use um dos tipos de mídia que você criou na etapa 1. Em geral, você deve usar o formato com a qualidade mais alta.
5.  Opcionalmente, de definir atributos no descritor de fluxo. Para ver uma lista de atributos que se aplicam a descritores de fluxo, consulte [Atributos do descritor de fluxo.](stream-descriptor-attributes.md)

Agora, crie o descritor de apresentação:

1.  Chame [**MFCreatePresentationDescriptor e**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) passe a matriz de descritores de fluxo. A função retorna um [**ponteiro IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
2.  Escolha a seleção de fluxo padrão chamando [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) para selecionar um ou mais fluxos. Pelo menos um fluxo deve ser selecionado na configuração padrão.
3.  Opcionalmente, de definir atributos no descritor de apresentação. Para ver uma lista de atributos que se aplicam a descritores de fluxo, consulte [Atributos do descritor de apresentação.](presentation-descriptor-attributes.md)

Você deve criar o descritor de apresentação uma vez, na inicialização ou depois que a origem tiver analisado o suficiente dos dados de origem para determinar o conteúdo. O [**método CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) deve retornar uma cópia do descritor de apresentação. Para criar a cópia, chame [**IMFPresentationDescriptor::Clone.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone) Retornar uma cópia impede que o cliente modifique o estado do descritor de apresentação original, como os atributos ou a seleção de fluxo. No entanto, esteja ciente de **que Clone** cria uma cópia superficial, para que o cliente possa modificar os descritores de fluxo subjacentes.

## <a name="starting-the-media-source"></a>Iniciando a fonte de mídia

O [**método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia a fonte de mídia ou busca uma nova posição. Uma chamada para **Iniciar** causa uma *busca* quando o estado anterior estava em pausa ou em execução e uma nova hora de início é especificada. Caso contrário, **o método Start** causará um *início*. Quando a **operação** Iniciar for concluída, envie os seguintes eventos.

1.  Envie um [evento MENewStream](menewstream.md) para cada novo fluxo, ou seja, cada fluxo que foi desleixado anteriormente e agora está selecionado. Os dados do evento são um ponteiro para o fluxo.
2.  Envie um [evento MEUpdatedStream](meupdatedstream.md) para cada fluxo que foi selecionado anteriormente e ainda está selecionado. Os dados do evento são um ponteiro para o fluxo. (Não envie um evento para fluxos deseletórios.)
3.  Se a origem estiver procurando, envie um [evento MESourceSeeked.](mesourceseeked.md) Caso contrário, envie [um evento MESourceStarted.](mesourcestarted.md) Os dados do evento são a hora de início especificada no [**método**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Start. Para o evento MESourceStarted, se a hora de início for VT EMPTY, de definido o atributo \_ [**MF \_ EVENT SOURCE \_ ACTUAL \_ \_ START**](mf-event-source-actual-start-attribute.md) no evento. O valor do atributo é a hora de início real.
4.  Para cada fluxo, se a origem estiver buscando, envie um [evento MEStreamSeeked.](mestreamseeked.md) Caso contrário, envie [um evento MEStreamStarted.](mestreamstarted.md) Os dados do evento são a hora de início. (A fonte de mídia pode enfilerar um evento no fluxo chamando o método [**IMFMediaEventGenerator::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) do fluxo.)

Quando um fluxo for deseletório, desligue o fluxo. O fluxo não deve enfil de mais eventos nesse ponto.

O formato de hora para [**o método Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é dado no parâmetro *pguidTimeFormat.* O formato de hora padrão, indicado por **GUID \_ NULL,** é de 100 unidades de nanossegundos. Uma fonte de mídia deve dar suporte a esse formato de hora.

### <a name="seeking"></a>Procurando

Ao buscar, a posição inicial solicitada pode não se enquadrar em um limite de exemplo exato. Além disso, para conteúdo compactado, a posição inicial pode ficar entre quadros-chave. Um fluxo deve fornecer amostras do ponto mais antigo necessário para produzir uma amostra descompactada na posição inicial solicitada. Para o vídeo, isso significa iniciar do quadro-chave anterior. O pipeline é responsável por soltar os quadros extras do decodificador, para que a reprodução seja iniciada no momento solicitado.

A hora de início determinada nos eventos de origem ([MESourceStarted,](mesourcestarted.md) [MESourceSeeked,](mesourceseeked.md) [MEStreamStarted](mestreamstarted.md)e [MEStreamSeeked](mestreamseeked.md)) é a hora de início solicitada (o valor dado no método [**Start),**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) independentemente da posição inicial real.

Por exemplo, suponha que os primeiros quadros de um fluxo de vídeo tenham as seguintes características:



| Amostra     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Hora       | 33 msec | 66 ms | 100 msec | 133 msec |
| Quadro-chave? | Sim     | Não      | Não       | Sim      |



 

Se o [**método Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) for chamado com um valor de 100 milissegundos, a origem precisará fazer a saída do vídeo do quadro 1, o primeiro quadro-chave antes desse momento. O evento de início ainda indicará 100 milissegundos nos dados do evento.

## <a name="pausing-the-media-source"></a>Pausando a fonte de mídia

O [**método IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) pausa a fonte de mídia.

Enquanto a origem está em pausa, um fluxo pode criar novos exemplos e armazená-los em uma fila, mas o fluxo não entrega os exemplos. Aqui estão algumas exceções a essa regra:

-   Fontes ao vivo devem soltar dados enquanto estão em pausa.
-   Se a origem obtém dados de uma rede, ela pode pausar o servidor.

Se o cliente chamar [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) enquanto a origem estiver em pausa, a solicitação também será en fila até que a origem seja iniciada novamente. As solicitações não devem ser descartados.

A pausa só é permitida no estado iniciado. Caso contrário, [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) deverá retornar **MF \_ E INVALID \_ \_ STATE \_ TRANSITION**.

## <a name="generating-source-data"></a>Gerando dados de origem

Media Foundation usa um *modelo de pull*, o que significa que os fluxos geram e entregam exemplos em resposta a solicitações do pipeline. Um fluxo pode fornecer exemplos quando a fonte de mídia está em execução e o fluxo é selecionado. Um fluxo fornece dados somente quando o cliente solicita um novo exemplo.

### <a name="sample-requests"></a>Solicitações de Amostra

O cliente solicita um novo exemplo chamando [**IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) Esta é a sequência de operações:

1.  O cliente chama [**IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) O argumento é um ponteiro para um objeto *de token* opcional que o cliente usa para acompanhar a solicitação. O cliente implementa o token. Os tokens devem expor a interface **IUnknown.** O cliente também pode passar um ponteiro NULL em vez de um token.
2.  Se o cliente forneceu um token, o fluxo de mídia chama **AddRef** no token e coloca o token em uma fila de entrada e primeira saída. O método retorna e as etapas restantes ocorrem de forma assíncrona.

3.  Quando mais dados estão disponíveis, o fluxo de mídia cria um novo exemplo. (Esta etapa é descrita em mais detalhes na próxima seção.)
4.  O fluxo de mídia recebe o primeiro token da fila.
5.  Se o token não for **NULL,** o fluxo de mídia define o atributo [**\_ Token MFSampleExtension**](mfsampleextension-token-attribute.md) no exemplo de mídia. O valor do atributo é um ponteiro para o token.
6.  O fluxo de mídia envia um [evento MEMediaSample.](memediasample.md) Os dados de evento são um ponteiro para a interface [**IMFSample do**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) exemplo.
7.  Se o cliente forneceu um token, o fluxo de mídia **chama Release** no objeto de token.

Se o fluxo de mídia não puder atender à solicitação [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) do cliente, ele esmaece o token da fila e chama **Release** no token, mas não envia um evento [MEMediaSample.](memediasample.md)

O cliente pode usar o token para acompanhar o status da solicitação. Quando o cliente recebe o [evento MEMediaSample,](memediasample.md) ele pode obter o token do exemplo e corresponder a ele com a solicitação original. O cliente também pode usar o token para detectar se a fonte de mídia descarrou a solicitação. Se a contagem de referência do token cair para zero e o fluxo de mídia não enviar um evento MEMediaSample, isso significa que a solicitação foi retirada.

As etapas listadas aqui pressupom [**que o método RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) é implementado como uma operação assíncrona. Se o método for síncrono, você não precisará colocar o token de solicitação em uma fila. No entanto, se a geração de dados levar algum tempo significativo, uma abordagem assíncrona será recomendada, por exemplo, se a origem ler dados de um fluxo de byte.

O fluxo é responsável por buffer de todos os dados acumulados entre chamadas para [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

Quando o fluxo de mídia atinge o final do fluxo, ele envia um [evento MEEndOfStream](meendofstream.md) após o último exemplo. Depois que cada fluxo terminar, a fonte de mídia enviará [um evento MEEndOfPresentation.](meendofpresentation.md) Depois que um fluxo de mídia envia o evento MEEndOfStream, o método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) retorna **MF \_ E END OF \_ \_ \_ STREAM** até que a origem seja reiniciada.

### <a name="allocating-samples"></a>Alocando exemplos

Quando o fluxo está pronto para preencher uma solicitação de exemplo pendente, ele cria um novo exemplo e adiciona um ou mais buffers de mídia ao exemplo. Para obter mais informações sobre como criar buffers de mídia, consulte [Buffers de mídia](media-buffers.md).

O fluxo deve definir o carimbo de data/hora e a duração, se conhecido. O carimbo de data/hora é relativo à origem. Na maioria dos casos, o início do conteúdo corresponde a um carimbo de data/hora de zero. Por exemplo, se a origem ler de um arquivo de mídia, o início do arquivo terá um carimbo de data/hora de zero.

O carimbo de data/hora no exemplo não é necessariamente igual ao tempo de apresentação. A Sessão de Mídia é traduzida da hora de origem para a hora da apresentação. Para dados compactados, o fluxo deve gerar dados começando no quadro-chave mais próximo antes da hora de início. Isso permite que o decodificador entregue o quadro que aparece na hora de início solicitada. (Caso contrário, o decodificador precisaria aguardar até o quadro-chave a seguir.)

Se a taxa de reprodução for mais rápida ou mais lenta que 1,0, o pipeline ajustará a taxa do relógio de apresentação. A origem não ajusta os carimbos de data/hora em exemplos.

A origem pode definir informações adicionais sobre o exemplo definindo atributos. Para ver uma lista de atributos de exemplo, consulte [Atributos de exemplo.](sample-attributes.md)

### <a name="gaps-in-the-stream"></a>Lacunas no fluxo

Se um fluxo contiver uma lacuna de comprimento significativo, é recomendável que o fluxo envie um [evento MEStreamTick.](mestreamtick.md) Esse evento notifica o cliente de que um exemplo está ausente. Os dados do evento são o carimbo de data/hora do exemplo ausente, em unidades de 100 nanossegundos (**VT \_ I8**). Esse evento pode salvar componentes downstream de aguardar amostras que não chegarão. O fluxo pode enviar quantos eventos MEStreamTick necessários para abranger a lacuna no fluxo.

## <a name="shutting-down-the-media-source"></a>Desligando a fonte de mídia

Quando o cliente terminar de usar a fonte de mídia, ele [**chamará IMFMediaSource::Shutdown.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) Dentro desse método, a fonte de mídia deve quebrar todas as contagens de referência circulares. Normalmente, haverá referências circulares entre a fonte de mídia e os fluxos de mídia.

Se você estiver usando a fila de eventos para implementar [**IMFMediaEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)chame [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) na fila de eventos. Esse método desliga a fila de eventos e sinaliza qualquer chamador que está aguardando um evento no momento.

Após o desligamento, todos os métodos na origem **retornam MF \_ E \_ SHUTDOWN**, com exceção dos **métodos IUnknown.**

## <a name="live-sources"></a>Fontes ao vivo

A partir do Windows 7, o Media Foundation automaticamente dá suporte a dispositivos de captura de áudio e vídeo. Para vídeo, o dispositivo deve fornecer um minidriver de streaming de kernel (KS) na categoria de captura de vídeo. Media Foundation usa o caminho PnP para enumerar o dispositivo. Para áudio, Media Foundation a API Windows DISPOSITIVO MULTIMÍDIA (MMDevice) para enumerar dispositivos de ponto de extremidade de áudio. Se o dispositivo atender a esses critérios, não será necessário implementar uma fonte de mídia personalizada.

No entanto, talvez você queira implementar uma fonte de mídia personalizada para algum outro tipo de dispositivo ou outra fonte de dados ao vivo. Há apenas algumas diferenças entre uma fonte ao vivo e outras fontes de mídia:

-   No método [**IMFMediaSource::GetCharacteristics,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) retorne o **sinalizador MFMEDIASOURCE \_ IS \_ LIVE.**
-   O primeiro exemplo deve ter um carimbo de data/hora de zero.
-   Eventos e estados de streaming são tratados da mesma forma que as fontes de mídia, com exceção do estado pausado.
-   Enquanto estiver em pausa, não enfile amostras. Solte todos os dados gerados durante a pausa.
-   As fontes ao vivo normalmente não têm suporte para busca, reprodução inversa ou controle de taxa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Tutorial: Escrevendo uma fonte de mídia personalizada](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



