---
description: Sobre filtros do DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Sobre filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550850"
---
# <a name="about-directshow-filters"></a>Sobre filtros do DirectShow

O DirectShow usa uma arquitetura modular, em que cada estágio de processamento é feito por um objeto COM chamado de filtro. O DirectShow fornece um conjunto de filtros padrão para aplicativos a serem usados, e os desenvolvedores podem escrever seus próprios filtros personalizados que estendem a funcionalidade do DirectShow. Para ilustrar, aqui estão as etapas necessárias para reproduzir um arquivo de vídeo AVI, juntamente com os filtros que executam cada etapa:

-   Leia os dados brutos do arquivo como um fluxo de bytes (filtro de origem de arquivo).
-   Examine os cabeçalhos AVI e analise o fluxo de bytes em quadros de vídeo e amostras de áudio separados (filtro de Splitter AVI).
-   Decodifique os quadros de vídeo (vários filtros de decodificador, dependendo do formato de compactação).
-   Desenhe os quadros de vídeo (filtro de processamento de vídeo).
-   Envie os exemplos de áudio para a placa de som (filtro de dispositivo DirectSound padrão).

Esses filtros são mostrados no diagrama a seguir.

![gráfico de filtro para reprodução de um arquivo AVI com vídeo compactado](images/avi-filter-graph.png)

Como mostra o diagrama, cada filtro é conectado a um ou mais filtros. Os pontos de conexão também são objetos COM, chamados *Pins*. Os filtros usam Pins para mover dados de um filtro para o próximo. As setas no diagrama mostram a direção na qual os dados viajam. No DirectShow, um conjunto de filtros é chamado de *gráfico de filtro*.

Os filtros têm três estados possíveis: em execução, parado e em pausa. Quando um filtro está em execução, ele processa os dados de mídia. Quando ele é interrompido, ele para de processar os dados. O estado em pausa é usado para a indicação de dados antes da execução; o fluxo de dados da seção [no gráfico de filtro](data-flow-in-the-filter-graph.md) descreve esse conceito em mais detalhes. Com exceções muito raras, as alterações de estado são coordenadas em todo o grafo de filtro; todos os filtros na opção de gráfico não são ativados. Assim, todo o gráfico de filtro também é considerado em execução, parado ou pausado.

Os filtros podem ser agrupados em várias categorias amplas:

-   Um filtro de *origem* introduz dados no grafo. Os dados podem vir de um arquivo, uma rede, uma câmera ou qualquer outro lugar. Cada filtro de origem manipula um tipo diferente de fonte de dados.
-   Um filtro de *transformação* usa um fluxo de entrada, processa os dados e cria um fluxo de saída. Codificadores e decodificadores são exemplos de filtros de transformação.
-   Os filtros de *renderização* ficam no final da cadeia. Eles recebem dados e apresentam a ele o usuário. Por exemplo, um processador de vídeo desenha quadros de vídeo na tela; um processador de áudio envia dados de áudio para a placa de som; e um filtro de gravador de arquivo grava dados em um arquivo.
-   Um filtro de *divisão* divide um fluxo de entrada em duas ou mais saídas, normalmente analisando o fluxo de entrada ao longo do caminho. Por exemplo, o divisor AVI analisa um fluxo de bytes em fluxos de áudio e vídeo separados.
-   Um filtro *MUX* usa várias entradas e as combina em um único fluxo. Por exemplo, o AVI Mux executa a operação inversa do divisor AVI. Ele usa fluxos de áudio e vídeo e produz um fluxo de bytes formatado em AVI.

As distinções entre essas categorias não são absolutas. Por exemplo, o filtro de leitor de ASF atua como um filtro de origem e um filtro de divisão.

Todos os filtros do DirectShow expõem a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e todos os Pins expõem a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . O DirectShow também define muitas outras interfaces que dão suporte a uma funcionalidade mais específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador do grafo de filtro](about-the-filter-graph-manager.md)
</dt> <dt>

[Fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



