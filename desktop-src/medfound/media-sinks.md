---
description: Os coletores de mídia são os objetos de pipeline que recebem dados de mídia.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Coletores de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297898"
---
# <a name="media-sinks"></a>Coletores de mídia

Os *coletores de mídia* são os objetos de pipeline que recebem dados de mídia. Um coletor de mídia é o destino de um ou mais fluxos de mídia. Os coletores de mídia se enquadram em duas categorias gerais:

-   Um *renderizador* é um coletor de mídia que apresenta dados para reprodução. O processador de vídeo avançado (EVR) exibe quadros de vídeo e o processador de áudio reproduz fluxos de áudio por meio da placa de som ou outro dispositivo de áudio.

-   Um *coletor de arquivo* é um coletor de mídia que grava dados em um arquivo ou outro armazenamento.

A principal diferença entre eles é que um coletor de arquivo morto não consome os dados em uma taxa de reprodução fixa. Em vez disso, ele grava os dados que recebe o mais rápido possível.

Os coletores de mídia expõem a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) . Cada coletor de mídia contém um ou mais *coletores de fluxo*. Cada coletor de fluxo recebe os dados de um fluxo. Os coletores de fluxo expõem a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Normalmente, um aplicativo não cria coletores de mídia diretamente. Em vez disso, o aplicativo cria um ou mais objetos de ativação, que a sessão de mídia usa para criar o coletor. Todas as outras operações no coletor são tratadas pela sessão de mídia e o aplicativo não chama nenhum método no coletor de mídia ou qualquer um dos coletores de fluxo. Para obter mais informações sobre objetos de ativação, consulte [Activation Objects](activation-objects.md).

Você deve ler o restante deste tópico se estiver escrevendo um coletor de mídia personalizado ou se quiser usar um coletor de mídia diretamente sem a sessão de mídia.

-   [Coletores de fluxo](#stream-sinks)
-   [Relógio de apresentação](#presentation-clock)
-   [Formatos de fluxo](#stream-formats)
-   [Fluxo de Dados](#data-flow)
-   [Marcadores](#markers)
-   [Alterações de estado](#state-changes)
-   [Finalizando](#finalizing)
-   [Desligando](#shutting-down)
-   [Interfaces de coletor de mídia](#media-sink-interfaces)
-   [Interfaces de coletor de fluxo](#stream-sink-interfaces)
-   [Eventos de coletor de fluxo](#stream-sink-events)
-   [Tópicos relacionados](#related-topics)

## <a name="stream-sinks"></a>Coletores de fluxo

Um coletor de mídia pode ter um número fixo de coletores de fluxo ou pode dar suporte à adição e remoção de coletores de fluxo. Se ele tiver um número fixo de coletores de fluxo, o método [**IMFMediaSink:: getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retornará o \_ sinalizador de fluxos fixos MEDIASINK \_ . Caso contrário, você pode adicionar e remover coletores de fluxo. Para adicionar um novo coletor de fluxo, chame [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Para remover um coletor de fluxo, chame [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). O \_ sinalizador de fluxos fixos MEDIASINK \_ indica que o coletor de mídia não dá suporte a esses dois métodos. (Ele pode dar suporte a alguma outra maneira de configurar o número de fluxos, por exemplo, definindo parâmetros de inicialização quando o coletor é criado.) A lista de coletores de fluxo é ordenada. Para enumerá-los por valor de índice, chame o método [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) .

Coletores de fluxo também têm identificadores. Os identificadores de fluxo são exclusivos no coletor de mídia, mas não precisam ser consecutivos. Dependendo do coletor de mídia, os identificadores de fluxo podem ter algum significado relacionado ao conteúdo. Por exemplo, um coletor de arquivos pode gravar os identificadores de fluxo no cabeçalho do arquivo. Caso contrário, eles são arbitrários. Para obter um coletor de fluxo por seu identificador, chame [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Relógio de apresentação

A taxa em que um coletor de mídia consome amostras é controlada pelo [relógio de apresentação](presentation-clock.md). A sessão de mídia seleciona o relógio de apresentação e o define no coletor de mídia chamando o método [**IMFMediaSink:: SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) do coletor de mídia. O relógio de apresentação deve ser definido no coletor de mídia antes que o streaming possa começar. Cada coletor de mídia requer um relógio de apresentação para ser executado. O coletor de mídia usa o relógio de apresentação para duas finalidades:

-   Para receber notificações quando o streaming iniciar ou parar. O coletor de mídia recebe essas notificações por meio da interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) , que todos os coletores de mídia devem implementar.

-   Para determinar quando ele deve renderizar exemplos. Quando o coletor de mídia recebe um novo exemplo, ele obtém o carimbo de data/hora do exemplo e tenta renderizar o exemplo nesse horário de apresentação.

O relógio de apresentação deriva seus horários de relógio de outro objeto chamado *fonte de tempo de apresentação*. As fontes de tempo de apresentação expõem a interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Alguns coletores de mídia têm acesso a um relógio preciso, portanto, expõem essa interface. Isso significa que um coletor de mídia pode agendar amostras em relação a um tempo fornecido por seu próprio relógio. No entanto, o coletor de mídia não pode pressupor que esse seja o caso. Ele sempre deve usar o tempo do relógio de apresentação, independentemente de o relógio de apresentação ser controlado pelo próprio coletor de mídia ou por algum outro relógio.

Se um coletor de mídia não corresponder a taxas com um relógio diferente de seu próprio, o método [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retornará o MEDIASINK \_ não poderá \_ corresponder ao sinalizador de \_ relógio. Se esse sinalizador estiver presente e o relógio de apresentação usar uma fonte de tempo de apresentação diferente, provavelmente o coletor de mídia será executado inadequadamente. Por exemplo, pode haver uma falha durante a reprodução.

Um coletor sem *taxa* é um coletor de mídia que ignora os carimbos de data/hora em exemplos e consome dados assim que cada amostra chega. Um coletor de mídia sem taxa retorna o \_ sinalizador MEDIASINK sem taxa do método [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Normalmente, esse sinalizador se aplica aos coletores de arquivo. Se cada coletor de mídia no pipeline for sem taxa, a sessão de mídia usará um relógio de apresentação de taxa especial. Esse relógio é executado tão rapidamente quanto os coletores consomem exemplos.

## <a name="stream-formats"></a>Formatos de fluxo

Antes que o coletor de mídia possa receber amostras, o cliente deve definir o tipo de mídia nos coletores de fluxo. Para definir o tipo de mídia, chame o método [**IMFStreamSink:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) do coletor de fluxo. Esse método retorna um ponteiro para a interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) . Use essa interface para obter a lista de tipos de mídia preferenciais, obter o tipo de mídia atual e definir o tipo de mídia.

Para obter a lista de tipos de mídia preferenciais, chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex). Os tipos preferenciais devem ser levados em uma dica ao cliente. A lista pode estar incompleta ou incluir tipos de mídia parciais. Um tipo de mídia parcial é aquele que não tem todos os atributos necessários para descrever um formato válido. Por exemplo, um tipo de vídeo parcial pode especificar o espaço de cores e a profundidade de bits, mas não a largura ou altura da imagem. Um tipo de áudio parcial pode especificar o formato de compactação e a taxa de amostra, mas não o número de canais de áudio.

Para obter o tipo de mídia atual do coletor de fluxo, chame [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Quando um coletor de fluxo é criado pela primeira vez, ele pode ter um tipo de mídia padrão já definido ou pode não ter nenhum tipo de mídia até que o cliente defina um.

Para definir o tipo de mídia, chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Alguns coletores de fluxo podem não dar suporte à alteração do tipo após ter sido definido. Portanto, é útil testar os tipos de mídia antes de defini-los. Para testar se o coletor de mídia aceitará um tipo de mídia (sem definir o tipo), chame [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Fluxo de Dados

Os coletores de mídia usam um *modelo de pull*, o que significa que os coletores de fluxo solicitam dados conforme eles precisam. O cliente deve responder em tempo hábil para evitar qualquer falha.

Alguns coletores de mídia dão suporte à *preversão*. A preversão é o processo de fornecer dados ao coletor de mídia antes do início do relógio de apresentação. Se um coletor de mídia der suporte à desdistribuição, o coletor de mídia expõe a interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) e o método [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retorna o \_ sinalizador MEDIASINK pode ser \_ prevertido. A preversão garante que o coletor de mídia esteja pronto para apresentar a primeira amostra quando o relógio de apresentação for iniciado. É recomendável que o cliente sempre seja prevertido se o coletor de mídia der suporte a ele, pois ele pode impedir falhas ou falhas durante a reprodução.

O fluxo de dados para um coletor de mídia funciona da seguinte maneira:

1.  O cliente define os tipos de mídia e o relógio de apresentação. O coletor de mídia se registra com o relógio de apresentação para receber notificações sobre alterações de estado do relógio.
2.  Opcionalmente, o cliente consulta para [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll). Se o coletor de mídia expõe essa interface, o cliente chama [**IMFMediaSinkPreroll:: NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll). Caso contrário, o cliente passará para a etapa 5.
3.  Cada coletor de fluxo envia um ou mais eventos [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . Em resposta a cada um desses eventos, o cliente obtém a próxima amostra de dados para esse fluxo e chama [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample).
4.  Quando cada coletor de fluxo recebe dados de preversão suficientes, ele envia um evento [MEStreamSinkPrerolled](mestreamsinkprerolled.md) .
5.  O cliente chama [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) para iniciar o relógio de apresentação.
6.  O relógio de apresentação notifica o coletor de mídia que o relógio está iniciando, chamando [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).
7.  Para obter mais dados, cada coletor de fluxo envia eventos [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . Em resposta a cada um desses eventos, o cliente obtém o próximo exemplo e chama [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample). Esta etapa é repetida até que a apresentação termine.

A maioria dos coletores de mídia processa amostras de forma assíncrona, portanto, os coletores de fluxo podem enviar mais de uma solicitação de exemplo por vez.

Durante o streaming, o cliente pode chamar [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) e [**IMFStreamSink:: flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) a qualquer momento. Os marcadores são descritos na próxima seção. A liberação faz com que o coletor de fluxo descarte quaisquer exemplos que tenha colocado na fila, mas que ainda não foram renderizados.

## <a name="markers"></a>Marcadores

Os marcadores fornecem uma maneira para o cliente indicar pontos específicos no fluxo. Um marcador consiste nas seguintes informações:

-   O tipo de marcador, definido como um membro da enumeração de [**\_ \_ tipo de marcador MFSTREAMSINK**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) .
-   Dados associados ao marcador. O significado dos dados depende do tipo de marcador. Alguns tipos de marcador não têm dados.
-   Dados opcionais para uso próprio do cliente.

Para inserir um marcador, o cliente chama [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker). O coletor de fluxo conclui o processamento de quaisquer exemplos recebidos antes da chamada **PlaceMarker** e, em seguida, envia um evento [MEStreamSinkMarker](mestreamsinkmarker.md) .

A maioria dos coletores de mídia mantém uma fila de amostras pendentes, que são processadas de forma assíncrona. Os eventos de marcador devem ser serializados com o processamento de exemplo, portanto, o coletor de mídia deve colocar os marcadores na mesma fila. Por exemplo, suponha que o cliente faça as seguintes chamadas de método:

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemplo \# 1)
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemplo \# 2)
3.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 1)
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemplo \# 3)
5.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 2)

Neste exemplo, o coletor de fluxo deve enviar o evento [MEStreamSinkMarker](mestreamsinkmarker.md) para o marcador \# 1 depois de processar a amostra \# 2 e o evento para o marcador \# 2 depois de processar a amostra \# 3.

Se o cliente liberar um coletor de fluxo, o coletor de fluxo processará imediatamente quaisquer marcadores que estavam na fila. Ele define o código de status como E \_ abortar nesses eventos.

Alguns marcadores contêm informações que são relevantes para o coletor de mídia:

-   **MFSTREAMSINK \_ \_Tique do marcador**: indica que há uma lacuna no fluxo. O próximo exemplo será uma descontinuidade.
-   **MFSTREAMSINK \_ \_ENDOFSEGMENT do marcador**: indica o fim de um segmento ou o fim de um fluxo. O próximo exemplo (se houver) pode ser uma descontinuidade.
-   **MFSTREAMSINK \_ \_Evento de marcador**: contém um evento. Dependendo do tipo de evento e da implementação do coletor de mídia, o coletor de mídia pode lidar com o evento ou ignorá-lo.

## <a name="state-changes"></a>Alterações de estado

Um coletor de mídia é notificado sobre alterações de estado no relógio de apresentação por meio da interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) do coletor de mídia. Quando o cliente define o relógio de apresentação, o coletor de mídia chama [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) para se registrar para notificações do relógio. A tabela a seguir resume como um coletor de mídia se comporta em resposta às alterações de estado do relógio.



| Alteração de estado do relógio                                         | Exemplo de processamento                                                                                                                                                                                                                                             | Processamento de marcador                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Os exemplos de processo cujo carimbo de data/hora é igual ou posterior à hora de início do relógio.                                                                                                                                                                              | Envie o evento [MEStreamSinkMarker](mestreamsinkmarker.md) quando todos os exemplos recebidos antes do marcador tiverem sido processados.                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | O coletor de mídia pode falhar [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) enquanto está em pausa.<br/> Se o coletor de mídia aceitar amostras enquanto estiver em pausa, ele deverá enfileirar-las até que o relógio seja reiniciado. Não processe nenhuma amostra em fila enquanto estiver em pausa.<br/> | Se houver amostras em fila, coloque marcadores na mesma fila. Enviar o evento de marcador quando o relógio for reiniciado.<br/> Caso contrário, envie o evento de marcador imediatamente.<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Processe quaisquer exemplos que foram enfileirados enquanto estavam em pausa e, em seguida, trate o mesmo que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).                                                                                                                         | Envie eventos [MEStreamSinkMarker](mestreamsinkmarker.md) para marcadores em fila (serializados com processamento de exemplo) e, em seguida, trate o mesmo que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Remova todas as amostras em fila. Outras chamadas para [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) podem falhar.                                                                                                                                                      | Enviar eventos de marcador na fila. Nas chamadas subsequentes para [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker), envie o evento de marcador imediatamente.                                                              |



 

Além disso, os coletores de fluxo devem enviar os seguintes eventos quando concluírem as transições de Estado:

-   Evento [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart): [MEStreamSinkStarted](mestreamsinkstarted.md)
-   [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause): evento [MEStreamSinkPaused](mestreamsinkpaused.md)
-   [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop): evento [MEStreamSinkStopped](mestreamsinkstopped.md)

## <a name="finalizing"></a>Finalizando

Alguns coletores de mídia exigem uma etapa de processamento extra após a última amostra ser entregue. Normalmente, esse requisito se aplica aos coletores de arquivo, que devem gravar cabeçalhos ou índices no arquivo. Se um coletor de mídia exigir qualquer processamento final, ele exporá a interface [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) .

Depois que o cliente entrega a última amostra, o cliente consulta essa interface. Se o coletor de mídia der suporte à interface, o cliente chamará [**IMFFinalizableMediaSink:: BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) para executar o processamento final de forma assíncrona. Esse método segue o modelo assíncrono de Media Foundation padrão, descrito em [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md). O coletor de mídia pode assumir que o cliente chamará **BeginFinalize**. A falha ao chamar **BeginFinalize** pode resultar em um arquivo criado incorretamente.

## <a name="shutting-down"></a>Desligando

Quando o cliente é concluído usando o coletor de mídia, o cliente chama [**IMFMediaSink:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown). Dentro desse método, o coletor de mídia deve interromper quaisquer contagens de referência circulares. Normalmente, haverá referências circulares entre o coletor de mídia e os coletores de fluxo.

Se você estiver usando o objeto auxiliar de fila de eventos para implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), chame [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) na fila de eventos. Esse método desliga a fila de eventos e sinaliza qualquer chamador que esteja aguardando um evento no momento.

Após o desligamento, todos os métodos no coletor de mídia retornam MF \_ E \_ Shutdown, com exceção dos métodos **IUnknown** .

## <a name="media-sink-interfaces"></a>Interfaces de coletor de mídia

A tabela a seguir lista as interfaces padrão que os coletores de mídia podem expor por meio de **QueryInterface**. Os coletores de mídia também podem expor interfaces personalizadas.



| Interface                                                      | Descrição                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | A interface primária para coletores de mídia. (Obrigatório.)                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Usado para notificar o coletor de mídia quando o relógio de apresentação muda de estado. (Obrigatório.)              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implemente se o coletor de mídia deve executar uma etapa de processamento final. (Opcional).                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implemente se o coletor de mídia expõe qualquer interface de serviço. (Opcional).                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implemente se o coletor de mídia envia qualquer evento. (Opcional).                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implemente se o coletor de mídia dá suporte a preversão. (Opcional).                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implemente se o coletor de mídia pode fornecer uma fonte de tempo para o relógio de apresentação. (Opcional). |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implemente se o coletor de mídia pode ajustar a qualidade da reprodução. (Opcional).                          |



 

Opcionalmente, um coletor de mídia pode implementar a interface como um serviço a seguir.



| Interface de serviço                        | Descrição                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Relata o intervalo de taxas de reprodução com suporte. |



 

Para obter mais informações sobre interfaces de serviço e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de serviço](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Interfaces de coletor de fluxo

Os coletores de fluxo devem expor as seguintes interfaces por meio de **QueryInterface**.



| Interface                                                | Descrição                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | A interface primária para coletores de fluxo. (Obrigatório.)                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Enfileira eventos. A interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) herda essa interface. (Obrigatório.) |



 

No momento, nenhuma interface de serviço é definida para coletores de fluxo.

## <a name="stream-sink-events"></a>Eventos de coletor de fluxo

A tabela a seguir lista os eventos que são definidos para coletores de fluxo genéricos. Coletores de fluxo também podem enviar eventos personalizados não listados aqui.



| Evento                                                                  | Descrição                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | O tipo de mídia do coletor de fluxo não é mais válido. (Opcional). |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | Um marcador foi processado. (Obrigatório.)                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | O coletor de fluxo foi pausado. (Obrigatório.)                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | A preversão foi concluída. (Opcional).                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | O coletor de fluxo alterou a taxa de reprodução. (Opcional).       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | Um novo exemplo é solicitado. (Obrigatório.)                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | Uma solicitação de limpeza foi concluída. (Opcional).                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | O coletor de fluxo foi iniciado. (Obrigatório.)                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | O coletor de fluxo foi interrompido. (Obrigatório.)                     |



 

Atualmente, nenhum evento de finalidade geral é definido para coletores de mídia. Alguns coletores de mídia podem enviar eventos personalizados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




