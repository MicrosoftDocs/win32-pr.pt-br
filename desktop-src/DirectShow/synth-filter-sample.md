---
description: Exemplo de filtro de sintetizador
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Exemplo de filtro de sintetizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a3a366a6612aadf653b5af13099dbc8a4f08c2fb828bca6e64514cb1801e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291186"
---
# <a name="synth-filter-sample"></a>Exemplo de filtro de sintetizador

## <a name="description"></a>Description

O filtro de sintetizador é um filtro de origem que gera ondas de áudio.

Esse filtro ilustra a criação dinâmica de gráficos. Ele pode alternar entre o áudio PCM não compactado e o formato compactado MS \_ ADPCM (modulação de código de pulso Delta da Microsoft).

Esse filtro aparece em GraphEdit como "filtro de sintetizador de áudio".

para obter mais informações sobre a criação dinâmica de grafo, consulte [dynamic Graph build](dynamic-graph-building.md).

## <a name="usage"></a>Uso

O filtro sintetizador permite que o usuário defina a forma de onda, a frequência, o número de canais e outras propriedades por meio da página de propriedades. Para definir o ponto de extremidade superior ou inferior do intervalo de frequência de removido, mantenha pressionada a tecla SHIFT enquanto ajusta o controle deslizante de frequência. O filtro também dá suporte a uma interface personalizada, ISynth2, para definir essas propriedades.

Para demonstrar o recurso de criação de gráfico dinâmico, faça o seguinte:

1.  Crie o filtro e registre-o com o utilitário regsvr32.
2.  Inicie o GraphEdit.
3.  Insira o filtro sintetizador de áudio. ele aparece na categoria filtros de DirectShow.
4.  Renderizar o pino de saída do filtro.
5.  Clique no botão **reproduzir** .
6.  Abra a página de propriedades do filtro.
7.  Na área formato de saída, selecione PCM ou Microsoft ADPCM.

## <a name="programming-notes"></a>Notas de programação

Este exemplo contém os seguintes arquivos:

-   Dynsrc. h, dynsrc. cpp: contém duas classes base para filtros de origem que dão suporte à criação de grafo dinâmico, CDynamicSource e CDynamicSourceStream.
-   ISynth. h: declara a interface ISynth2 personalizada para definir propriedades no filtro.
-   Resource. h: contém constantes de recurso.
-   Sintetizador. def: exporta as funções de DLL necessárias para a biblioteca COM.
-   Sintetizador. h, sintetizador. cpp: contém a classe CAudioSynth, que gera os dados de áudio e a classe CSynthFilter, que implementa o filtro.
-   Sintetizador. rc: contém recursos usados pelo filtro.
-   Synthprp. h, Synthprp. cpp: implementa a página de propriedades do filtro.

A classe CDynamicSource é adaptada da classe base [**CSource**](csource.md) . Ele usa um ou mais Pins de saída derivados da classe CDynamicSourceStream. A classe CDynamicSourceStream é adaptada da classe [**CSourceStream**](csourcestream.md) , mas deriva da classe [**CDynamicOutputPin**](cdynamicoutputpin.md) em vez da classe [**CBaseOutputPin**](cbaseoutputpin.md) .

A classe CDynamicSource tem os seguintes métodos não encontrados em [**CSource**](csource.md):

-   Stop: sinaliza o evento de parada ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) e desliga o thread de trabalho para todos os Pins não conectados. Em um PIN conectado, o método inativo do PIN desligará o thread de trabalho.
-   Pausa: redefine o evento de parada.
-   JoinFilterGraph: chama o método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) em cada PIN.

A classe CDynamicSourceStream tem os seguintes métodos não encontrados em [**CSourceStream**](csourcestream.md):

-   DestroySourceThread: desliga o thread de trabalho.
-   FatalError: sinaliza um erro para o Gerenciador do grafo de filtro.
-   OutputPinNeedsToBeReconnected: sinaliza que o pino de saída deve ser reconectado. Quando esse método é chamado, o thread de trabalho chama o método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para reconectar o PIN.

## <a name="downloading-the-sample"></a>Baixando o exemplo

para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow filtros de \\ \\ sintetizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



