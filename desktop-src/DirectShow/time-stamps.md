---
description: Carimbos de Data/Hora
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Carimbos de Data/Hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed14f0155a0bfbf209719f4aff97cbbd19501e6aa32d57e9f0c1cbb2df0964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072310"
---
# <a name="time-stamps"></a>Carimbos de Data/Hora

O *carimbo de data/hora* define as horas de início e término de um exemplo de mídia, medido em tempo de fluxo. O carimbo de data/hora é, às vezes, chamado de *tempo de apresentação*. Ao ler o restante deste artigo, é importante lembrar que nem todos os formatos usam carimbos de data/hora da mesma maneira. Por exemplo, nem todas as amostras MPEG são carimbadas por tempo. Em gráficos de filtro MPEG, o carimbo de data/hora não é aplicado a cada quadro até que eles sejam impressos do decodificador.

Quando um filtro de renderizador recebe um exemplo, ele agenda a renderização com base no carimbo de data/hora. Se o exemplo chegar atrasado ou não tiver carimbo de data/hora, o filtro renderizará o exemplo imediatamente. Caso contrário, o filtro aguardará até a hora de início da amostra antes de renderizar o exemplo. (Ele aguarda a hora de início chamando o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .)

Filtros de origem e filtros do analisador são responsáveis por definir os carimbos de data/hora corretos nos exemplos que eles processam. Use as diretrizes a seguir.

-   Reprodução de arquivo: a primeira amostra é a hora carimbada com uma hora de início igual a zero. Os carimbos de data/hora subsequentes são determinados pelo tamanho da amostra e pela taxa de reprodução, que é determinada pelo formato de arquivo. O filtro que analisa o arquivo é responsável por calcular os carimbos de data/hora corretos (por exemplo, o [divisor AVI](avi-splitter-filter.md)).
-   Captura de vídeo e áudio: cada amostra é o tempo marcado com uma hora de início igual ao tempo de transmissão quando foi capturado, com as seguintes advertências:
    -   Os quadros de vídeo de um pino de visualização (em oposição a um PIN de captura) não são marcados com o tempo. Devido à latência do grafo, um quadro de vídeo que é carimbado com o tempo de captura sempre chegará ao final do processador de vídeo. Isso pode fazer com que o renderizador descarte os quadros, em uma tentativa de controle de qualidade. Para obter informações sobre o controle de qualidade, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).
    -   Captura de áudio: o filtro de captura de áudio usa seu próprio conjunto de buffers, que são separados daqueles usados pelo driver de áudio. O driver de áudio preenche os buffers do filtro de captura em intervalos fixos. O intervalo depende do driver, mas geralmente não tem mais de 10 milissegundos. Os carimbos de data/hora nos exemplos de áudio refletem a hora em que o driver preencheu os buffers do filtro de captura de áudio. Esses horários podem ser um pouco imprecisos, especialmente se o aplicativo estiver usando um tamanho de buffer muito pequeno. No entanto, os horários de mídia refletirão com precisão o número de amostras de áudio no buffer.
-   Filtros MUX: dependendo do formato de saída, um filtro Mux pode precisar gerar carimbos de data/hora ou talvez não. Por exemplo, o formato de arquivo AVI usa uma taxa de quadros fixa sem carimbos de data/hora, portanto, o filtro [AVI Mux](avi-mux-filter.md) assume que as amostras chegam em aproximadamente a hora certa. No entanto, se os carimbos de hora de entrada mostrarem uma lacuna maior do que um quadro, o AVI Mux gravará uma entrada de índice com o tamanho zero, para indicar um quadro Descartado. Na reprodução do arquivo, novos carimbos de data/hora são gerados em tempo de execução, conforme descrito anteriormente.

Para definir o carimbo de data/hora em um exemplo, chame o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

**Horários de mídia**

Opcionalmente, o filtro também pode especificar um *tempo de mídia* para o exemplo. Em um fluxo de vídeo, o tempo de mídia representa o número do quadro. Em um fluxo de áudio, o tempo de mídia representa o número de exemplo no pacote. Por exemplo, se cada pacote contiver um segundo áudio de 44,1 kilohertz (kHz), o primeiro pacote terá uma hora de início de mídia igual a zero e uma hora de parada de mídia de 44100. Em um fluxo pesquisável, o tempo de mídia é sempre relativo à hora de início do fluxo. Por exemplo, suponha que você busque 2 segundos desde o início de um fluxo de vídeo de 15 fps. O primeiro exemplo de mídia após a busca tem um carimbo de data/hora igual a zero, mas um tempo de mídia de 30.

Os filtros de renderizador e MUX podem usar o tempo de mídia para determinar se os quadros ou amostras foram descartados, verificando se há lacunas. No entanto, os filtros não são necessários para definir o tempo de mídia. Para definir o tempo de mídia em um exemplo, chame o método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



