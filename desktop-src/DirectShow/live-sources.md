---
description: Fontes dinâmicas
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Fontes dinâmicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8872cc5489ae61f3b7b9629e97303ad033630346094f8f1faa013f5da81d9142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153194"
---
# <a name="live-sources"></a>Fontes dinâmicas

Uma fonte ao vivo, também chamada de *fonte Push*, recebe dados em tempo real. Os exemplos incluem captura de vídeo e difusões de rede. Em geral, uma fonte dinâmica não pode controlar a taxa na qual os dados chegam.

Um filtro é considerado uma fonte ao vivo se uma das seguintes opções for verdadeira:

-   O filtro retorna os \_ sinalizadores diversos do filtro am \_ é o \_ \_ \_ sinalizador de origem do método [**IAMFilterMiscFlags:: GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) e pelo menos um de seus PINs de saída expõe a interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) .
-   O filtro expõe a interface [**IKsPropertySet**](ikspropertyset.md) e tem um PIN de captura (fixar \_ categoria \_ Capture). Consulte [fixar conjunto de propriedades](pin-property-set.md) para obter mais informações.

se um filtro de origem ao vivo fornecer um relógio, o filtro Graph Manager preferirá esse relógio quando escolher o relógio de referência do grafo. Consulte [relógios de referência](reference-clocks.md) para obter mais informações.

**Latência**

A latência de um filtro é a quantidade de tempo que leva para o filtro processar um exemplo. Para fontes dinâmicas, a latência é determinada pelo tamanho do buffer usado para manter amostras. Por exemplo, suponha que o grafo de filtro tenha uma fonte de vídeo com uma latência de 33 milissegundos (MS) e uma fonte de áudio com uma latência de 500 ms. Cada quadro de vídeo chega no processador de vídeo cerca de 470 MS antes da amostra de áudio correspondente atingir o processador de áudio. A menos que o grafo compensasse a diferença, o áudio e o vídeo não serão sincronizados.

As fontes dinâmicas podem ser sincronizadas por meio da interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . o filtro Graph Manager não sincroniza fontes dinâmicas, a menos que o aplicativo habilite a sincronização chamando o método [**IAMGraphStreams:: SyncUsingStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) . se a sincronização estiver habilitada, o filtro Graph gerenciador consultará cada filtro de origem para **IAMPushSource**. se o filtro der suporte a **IAMPushSource**, o filtro Graph Manager chamará [**IAMLatency:: getlatência**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) para recuperar a latência esperada do filtro. (A interface **IAMPushSource** herda [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency).) dos valores de latência combinados, o filtro Graph Manager determina a latência máxima esperada no grafo. Em seguida, ele chama [**IAMPushSource:: SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) para dar a cada filtro de origem um deslocamento de fluxo, que o filtro adiciona aos carimbos de data/hora que ele gera.

Esse método destina-se principalmente à visualização dinâmica. No entanto, observe que um pino de visualização em um dispositivo de captura ao vivo (como uma câmera) não define carimbos de data/hora nas amostras que ele fornece. Portanto, para usar esse método com um dispositivo de captura ao vivo, você deve Visualizar a partir do PIN de captura. para obter mais informações, consulte [DirectShow filtros de captura de vídeo](directshow-video-capture-filters.md).

Atualmente, a interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) é suportada pelo filtro de [captura VFW](vfw-capture-filter.md) e pelo filtro de [captura de áudio](audio-capture-filter.md) .

**Correspondência de taxa**

Se um filtro de processador agendar amostras usando um relógio de referência, mas o filtro de origem os produzir usando um relógio diferente, poderão ocorrer problemas na reprodução. O renderizador pode ser executado mais rápido do que a origem, causando lacunas nos dados. Ou pode ser executado de forma mais lenta do que a origem, fazendo com que as amostras "se montem" até, em algum momento, o grafo descartará os exemplos. Normalmente, uma fonte dinâmica não pode controlar sua taxa de produção e, portanto, o renderizador deve corresponder a taxas com a origem.

Atualmente, somente o processador de áudio executa a correspondência de taxa, pois os problemas na reprodução de áudio são mais perceptíveis do que os problemas em vídeo. Para executar a correspondência de taxa, o processador de áudio deve selecionar algo no qual ele corresponderá às taxas. Ele usa o seguinte algoritmo:

-   Se o grafo não estiver usando um relógio de referência, o processador de áudio não tentará corresponder as taxas. (Sempre que o grafo não tem um relógio de referência, os exemplos são sempre renderizados imediatamente à medida que chegam.)
-   Caso contrário, se houver um relógio de referência para o grafo, o processador de áudio verificará se há um upstream de origem ao vivo, usando os critérios descritos anteriormente. Caso contrário, o processador de áudio não corresponde às taxas.
-   Se houver um upstream de origem ao vivo e essa origem expor a interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) em seu pino de saída, o processador de áudio chamará [**IAMPushSource:: GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Ele procura um dos seguintes sinalizadores:
    -   \_PUSHSOURCECAPS \_ Internal \_ RM. Esse sinalizador significa que o filtro de origem tem seu próprio mecanismo de correspondência de taxa, portanto, o processador de áudio não corresponde às taxas.
    -   \_PUSHSOURCECAPS \_ não está \_ online. Esse sinalizador significa que o filtro de origem não é realmente uma fonte ao vivo, embora exponha a interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Portanto, o processador de áudio não corresponde às taxas.
    -   \_relógio PUSHSOURCECAPS \_ particular \_ . Esse sinalizador significa que o filtro de origem está usando um relógio privado para gerar carimbos de data/hora. Nesse caso, o renderizador de áudio corresponde às taxas em relação aos carimbos de data/hora. (Se os exemplos não tiverem carimbos de data/hora, o renderizador ignorará esse sinalizador.)
-   Se [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) não retornar nenhum sinalizador (zero), o comportamento do processador de áudio dependerá do relógio do grafo e se os exemplos têm carimbos de data/hora:
    -   Se o processador de áudio não for o relógio do grafo e os exemplos tiverem carimbos de data/hora, o renderizador de áudio corresponderá às taxas nos carimbos de data/hora.
    -   Se os exemplos não tiverem carimbos de data/hora, o processador de áudio tentará corresponder à taxa de dados de áudio de entrada.
    -   Se o processador de áudio for o relógio do grafo, ele tentará corresponder à taxa de dados de entrada.

O motivo do último caso é o seguinte: se o processador de áudio for o relógio de referência e o filtro de origem estiver usando o mesmo relógio para gerar carimbos de data/hora, o processador de áudio não poderá corresponder as taxas em relação aos carimbos de data/hora. Se tiver feito isso, em vigor, ele estaria tentando corresponder as taxas, o que poderia fazer com que o relógio fosse descompasso. Portanto, nesse caso, o renderizador corresponde à taxa de dados de áudio de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



