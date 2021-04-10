---
description: Este tópico descreve como os objetos de pipeline personalizados podem dar suporte a taxas de reprodução de variáveis, incluindo reprodução reversa. Para obter informações sobre como usar o controle de taxa de um aplicativo, consulte controle de taxa.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementando o controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011406"
---
# <a name="implementing-rate-control"></a>Implementando o controle de taxa

Este tópico descreve como os objetos de pipeline personalizados podem dar suporte a taxas de reprodução de variáveis, incluindo reprodução reversa. Para obter informações sobre como usar o controle de taxa de um aplicativo, consulte [controle de taxa](rate-control.md).

Este tópico contém as seguintes seções:

-   [Fontes de mídia](#media-sources)
-   [Transformações de Media Foundation](#media-foundation-transforms)
    -   [Reprodução reversa](#reverse-playback)
-   [Coletores de mídia](#media-sinks)
-   [Tópicos relacionados](#related-topics)

Se você estiver escrevendo um objeto de pipeline de Microsoft Media Foundation (uma origem de mídia, uma transformação ou um coletor de mídia), talvez seja necessário dar suporte a taxas de reprodução de variáveis. Para fazer isso, implemente as seguintes interfaces:

1.  Implemente a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Suporte ao serviço de **\_ \_ controle \_ de taxa de MF** . (Consulte [interfaces de serviço](service-interfaces.md).)
3.  Implemente a interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , que obtém as taxas de reprodução com suporte do objeto.
4.  Implemente a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) , que Obtém ou define a taxa de reprodução.

## <a name="media-sources"></a>Fontes de mídia

Se uma fonte de mídia der suporte ao controle de taxa, ela deverá implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Caso contrário, a sessão de mídia informa que a taxa mínima e máxima de reprodução é 1,0, independentemente de quais outros componentes estão no pipeline.

A taxa de reprodução não afeta os tempos de apresentação dos exemplos, portanto, a origem da mídia não deve ajustar seus carimbos de data/hora. Em vez disso, o relógio de apresentação é executado em uma velocidade mais rápida ou mais lenta. Para reprodução reversa, a origem fornece amostras na ordem inversa, com carimbos de data/hora decrescentes.

O parâmetro *fThin* do método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) indica se a origem da mídia deve *esfinar* o conteúdo. O finamento se aplica principalmente a fluxos de vídeo. No modo fino, a origem descarta os quadros Delta e entrega apenas os quadros-chave. Em taxas de reprodução muito altas, a origem pode ignorar alguns quadros-chave (por exemplo, entregar todos os outros quadros-chave).

A origem não precisa descartar amostras de áudio no modo fino. No entanto, em taxas de reprodução muito altas, a origem pode não ser capaz de ler os dados com rapidez nough para preencher as solicitações de exemplo do pipeline. Nesse caso, a origem pode precisar remover alguns dados de áudio. Nesse caso, ele deve tentar entregar amostras de áudio que estão próximas no tempo para os exemplos de vídeo (supondo que a origem tenha os dois tipos de fluxo).

Quando um fluxo faz a transição entre o modo fino e não fino, ele envia um evento [MEStreamThinMode](mestreamthinmode.md) .

Quando a origem da mídia conclui uma chamada para [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate), ela envia o evento [MESourceRateChanged](mesourceratechanged.md) .

Durante a reprodução reversa:

-   A origem da mídia fornece amostras na ordem inversa, sem ajustar os carimbos de data/hora.
-   Carimbos de data/hora em um fluxo devem diminuir de forma monotônico.
-   O início do conteúdo é considerado o fim do fluxo. Depois que cada fluxo de mídia entrega o primeiro exemplo no fluxo (ou seja, o tempo de apresentação = 0), ele envia o evento [MEEndOfStream](meendofstream.md) .

## <a name="media-foundation-transforms"></a>Transformações de Media Foundation

Em geral, uma Media Foundation de transformação (MFT) não precisa de suporte explícito para o controle de taxa, a menos que a MFT implemente a reprodução reversa não-finada.

Se uma MFT não implementar a interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , a sessão de mídia assumirá o seguinte:

-   A MFT dá suporte a taxas de reprodução de arbitrário para reprodução de encaminhamento, finas e não finas.
-   O MFT dá suporte à reprodução revertida fina, mas não oferece suporte à reprodução reversa não-finada.

Se uma dessas condições não for verdadeira, o MFT deverá implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).

### <a name="reverse-playback"></a>Reprodução reversa

A sessão de mídia pode ser revertida mesmo que uma ou mais transformações no pipeline não ofereçam suporte explicitamente à reprodução inversa.

Se uma MFT não expõe a interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , a sessão de mídia usa o *finamento* para reprodução reversa, da seguinte maneira:

-   A sessão de mídia envia quadros-chave para o MFT da maneira usual, chamando [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   A sessão de mídia descarta os quadros Delta e os substitui pelos eventos [MEStreamTick](mestreamtick.md) .

-   Entre cada exemplo, a sessão de mídia libera o MFT para evitar erros causados pelo fato de que os carimbos de data/hora estão diminuindo.

Um exemplo é considerado um quadro-chave se ele tiver o atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) definido como **true** e será considerado um quadro Delta se esse atributo for **false** ou não estiver definido.

Se o MFT implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport), a sessão de mídia usará essa interface para descobrir se o MFT dá suporte à reprodução reversa não-finada. Se o MFT der suporte à reprodução inversa não-finada, a sessão de mídia entregará todos os exemplos, na ordem inversa, sem descartar amostras ou liberar o MFT.

Se uma MFT oferecer suporte à reprodução inversa não fina, ela deverá implementar a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . A sessão de mídia usará essa interface para notificar o MFT quando ocorrer a reprodução reversa. Nesse ponto, o MFT deve estar preparado para os carimbos de data/hora a serem reduzidos e para que os quadros Delta cheguem em ordem inversa. Um decodificador normalmente precisará armazenar amostras em buffer até que tenha recebido um grupo inteiro de imagens (GOP) e, em seguida, decodificar toda a GOP e gerar os quadros decodificados na ordem correta (inversa).

## <a name="media-sinks"></a>Coletores de mídia

Se um coletor de mídia for sem *taxa*, a sessão de mídia assumirá que o coletor de mídia pode lidar com qualquer taxa de reprodução. O coletor de mídia não precisa implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). (Um coletor de mídia sem tarifas retorna o MEDIASINK \_ Sinalizador sem taxa do método [**IMFMediaSink:: getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) .)

Caso contrário, um coletor de mídia deve implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) se puder lidar com as taxas de reprodução diferentes de 1,0.

Os coletores de mídia não devem implementar [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Quando a taxa de reprodução é alterada, o relógio da apresentação chama o método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do coletor de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, avanço rápido e reprodução reversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



