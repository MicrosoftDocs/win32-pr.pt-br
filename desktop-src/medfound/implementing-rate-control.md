---
description: Este tópico descreve como objetos de pipeline personalizados podem dar suporte a taxas de reprodução de variáveis, incluindo reprodução inversa. Para obter informações sobre como usar o controle de taxa de um aplicativo, consulte Controle de taxa.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementando o controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3ff90e7b1748efd4cfcff41244164d1d6a997b6208d3e46afa0cdae9aa6bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114266"
---
# <a name="implementing-rate-control"></a>Implementando o controle de taxa

Este tópico descreve como objetos de pipeline personalizados podem dar suporte a taxas de reprodução de variáveis, incluindo reprodução inversa. Para obter informações sobre como usar o controle de taxa de um aplicativo, consulte [Controle de taxa](rate-control.md).

Este tópico contém as seguintes seções:

-   [Fontes de mídia](#media-sources)
-   [Media Foundation transformação](#media-foundation-transforms)
    -   [Reprodução inversa](#reverse-playback)
-   [Sinks de mídia](#media-sinks)
-   [Tópicos relacionados](#related-topics)

Se você estiver escrevendo um objeto Microsoft Media Foundation pipeline (uma fonte de mídia, transformação ou um sink de mídia), talvez seja necessário dar suporte a taxas de reprodução variável. Para fazer isso, implemente as seguintes interfaces:

1.  Implemente a interface [**IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Suporte ao **serviço MF \_ RATE CONTROL \_ \_ SERVICE.** (Consulte [Interfaces de Serviço](service-interfaces.md).)
3.  Implemente a interface [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) que obtém as taxas de reprodução compatíveis com o objeto .
4.  Implemente a interface [**IMFRateControl,**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) que obtém ou define a taxa de reprodução.

## <a name="media-sources"></a>Fontes de mídia

Se uma fonte de mídia dá suporte ao controle de taxa, ela deve implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Caso contrário, a Sessão de Mídia informa que a taxa de reprodução mínima e máxima é 1,0, independentemente de quais outros componentes estão no pipeline.

A taxa de reprodução não afeta os tempos de apresentação dos exemplos, portanto, a fonte de mídia não deve ajustar seus carimbos de data/hora. Em vez disso, o relógio de apresentação é executado em uma velocidade mais rápida ou mais lenta. Para reprodução inversa, a origem fornece exemplos em ordem inversa, com carimbos de data/hora decrescentes.

O *parâmetro fThin* do [**método IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) indica se a fonte de mídia deve *afinar* o conteúdo. O afinamento se aplica principalmente a fluxos de vídeo. No modo afinado, a origem descarta quadros delta e entrega apenas quadros-chave. Com taxas de reprodução muito altas, a origem pode ignorar alguns quadros-chave (por exemplo, entregar todos os outros quadros-chave).

A origem não precisa soltar amostras de áudio no modo fino. No entanto, com taxas de reprodução muito altas, a origem pode não conseguir ler dados rapidamente para preencher as solicitações de exemplo do pipeline. Nesse caso, a origem pode precisar soltar alguns dados de áudio. Nesse caso, ele deve tentar entregar amostras de áudio que estão próximas a tempo dos exemplos de vídeo (supondo que a origem tenha ambos os tipos de fluxo).

Quando um fluxo faz a transição entre o modo fino e não fino, ele envia um [evento MEStreamThinMode.](mestreamthinmode.md)

Quando a fonte de mídia conclui uma chamada para [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate), ela envia o [evento MESourceRateChanged.](mesourceratechanged.md)

Durante a reprodução inversa:

-   A fonte de mídia fornece exemplos em ordem inversa, sem ajustar os carimbos de data/hora.
-   Os carimbos de data/hora dentro de um fluxo devem diminuir de forma monotônica.
-   O início do conteúdo é considerado o final do fluxo. Depois que cada fluxo de mídia entregar o primeiro exemplo no fluxo (ou seja, o tempo de apresentação = 0), ele enviará o [evento MEEndOfStream.](meendofstream.md)

## <a name="media-foundation-transforms"></a>Media Foundation transformação

Em geral, uma transformação Media Foundation (MFT) não precisa de suporte explícito para o controle de taxa, a menos que o MFT implemente reprodução inversa não fina.

Se um MFT não implementar a interface [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) a Sessão de Mídia assumirá o seguinte:

-   O MFT dá suporte a taxas de reprodução arbitrárias para reprodução de encaminhamento, tanto emagressadas quanto não emagredas.
-   O MFT dá suporte à reprodução inversa fina, mas não dá suporte à reprodução inversa não fina.

Se qualquer uma dessas condições não for verdadeira, o MFT deverá implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

### <a name="reverse-playback"></a>Reprodução inversa

A Sessão de Mídia pode ser reproduzida em ordem inversa, mesmo que uma ou mais transformaçãos no pipeline não deem suporte explícito à reprodução inversa.

Se um MFT não expor a interface [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) a Sessão de Mídia usará a *afinação* para reprodução inversa, da seguinte forma:

-   A Sessão de Mídia envia quadros-chave para o MFT da maneira normal, chamando [**IMFTransform::P rocessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)

-   A Sessão de Mídia descarta quadros delta e os substitui por [eventos MEStreamTick.](mestreamtick.md)

-   Entre cada exemplo, a Sessão de Mídia libera o MFT, para evitar erros causados pelo fato de que os carimbos de data/hora estão diminuindo.

Um exemplo será considerado um quadro-chave se tiver o atributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) definido como **TRUE** e for considerado um quadro delta se esse atributo for **FALSE** ou não for definido.

Se o MFT implementar [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)a Sessão de Mídia usará essa interface para descobrir se o MFT dá suporte à reprodução inversa não fina. Se o MFT oferecer suporte à reprodução inversa não fina, a Sessão de Mídia entregará todos os exemplos, em ordem inversa, sem soltar amostras ou liberar a MFT.

Se uma MFT dá suporte à reprodução inversa não fina, ela deve implementar a interface [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) A Sessão de Mídia usará essa interface para notificar o MFT quando ocorrer reprodução inversa. Nesse ponto, o MFT deve estar preparado para que os carimbos de data/hora diminuam e para que os quadros delta cheguem em ordem inversa. Um decodificador normalmente precisará buffer de exemplos até que ele tenha recebido um GRUPO inteiro de imagens (GOP), decodificar todo o GOP e decodificar os quadros decodificados na ordem correta (inversa).

## <a name="media-sinks"></a>Sinks de mídia

Se um sink de mídia for *rateless*, a Sessão de Mídia assumirá que o sink de mídia pode lidar com qualquer taxa de reprodução. O sink de mídia não precisa implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). (Um sink de mídia sem taxa retorna o MEDIASINK \_ Sinalizador RATELESS do [**método IMFMediaSink::GetCharacteristics.)**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)

Caso contrário, um sink de mídia deverá implementar [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) se puder lidar com taxas de reprodução diferentes de 1,0.

Os sinks de mídia não devem implementar [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Quando a taxa de reprodução muda, o relógio de apresentação chama o método [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do sink de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, Avançar e reprodução inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



