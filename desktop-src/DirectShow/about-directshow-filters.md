---
description: Sobre DirectShow filtros
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Sobre DirectShow filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef947fdcec8cc1c01d23d09bce1b46d5b4d7d2268fe1d7cd6df6a57b54d42ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664457"
---
# <a name="about-directshow-filters"></a>Sobre DirectShow filtros

DirectShow usa uma arquitetura modular, em que cada estágio de processamento é feito por um objeto COM chamado filtro. DirectShow fornece um conjunto de filtros padrão para os aplicativos usarem e os desenvolvedores podem escrever seus próprios filtros personalizados que estendem a funcionalidade de DirectShow. Para ilustrar, aqui estão as etapas necessárias para reproduzir um arquivo de vídeo AVI, juntamente com os filtros que executam cada etapa:

-   Leia os dados brutos do arquivo como um fluxo de byte (filtro fonte de arquivo).
-   Examine os headers AVI e examine o fluxo de byte em quadros de vídeo e amostras de áudio separadas (filtro divisor AVI).
-   Decodificar os quadros de vídeo (vários filtros de decodificador, dependendo do formato de compactação).
-   Desenhar os quadros de vídeo (filtro do Renderador de Vídeo).
-   Envie os exemplos de áudio para a placa de som (filtro Padrão do Dispositivo DirectSound).

Esses filtros são mostrados no diagrama a seguir.

![grafo de filtro para reprodução de um arquivo avi com vídeo compactado](images/avi-filter-graph.png)

Como mostra o diagrama, cada filtro está conectado a um ou mais filtros. Os pontos de conexão também são objetos COM, chamados *de pinos*. Os filtros usam pinos para mover dados de um filtro no próximo. As setas no diagrama mostram a direção na qual os dados viajam. No DirectShow, um conjunto de filtros é chamado de *grafo de filtro*.

Os filtros têm três estados possíveis: em execução, parado e em pausa. Quando um filtro está em execução, ele processa dados de mídia. Quando ele é interrompido, ele interrompe o processamento de dados. O estado em pausa é usado para indicação de dados antes da execução; a seção [Dados Flow no filtro Graph](data-flow-in-the-filter-graph.md) descreve esse conceito mais detalhadamente. Com exceções muito raras, as alterações de estado são coordenadas em todo o grafo de filtro; todos os filtros nos estados da opção de grafo em uníson. Portanto, todo o grafo de filtro também é dito como em execução, parado ou em pausa.

Os filtros podem ser agrupados em várias categorias amplas:

-   Um *filtro* de origem introduz dados no grafo. Os dados podem vir de um arquivo, uma rede, uma câmera ou qualquer outro lugar. Cada filtro de origem lida com um tipo diferente de fonte de dados.
-   Um *filtro* de transformação recebe um fluxo de entrada, processa os dados e cria um fluxo de saída. Codificadores e decodificadores são exemplos de filtros de transformação.
-   *Os filtros* de renderização ficam no final da cadeia. Eles recebem dados e os apresentam ao usuário. Por exemplo, um renderador de vídeo desenha quadros de vídeo na exibição; um renderdor de áudio envia dados de áudio para a placa de som; e um filtro de file-writer grava dados em um arquivo.
-   Um *filtro divisor* divide um fluxo de entrada em duas ou mais saídas, normalmente analisado o fluxo de entrada ao longo do caminho. Por exemplo, o Divisor AVI analisará um fluxo de byte em fluxos de áudio e vídeo separados.
-   Um *filtro mux* recebe várias entradas e as combina em um único fluxo. Por exemplo, o AVI Mux executa a operação inversa do divisor AVI. Ele aceita fluxos de áudio e vídeo e produz um fluxo de byte formatado em AVI.

As distinções entre essas categorias não são absolutas. Por exemplo, o filtro Leitor do ASF atua como um filtro de origem e um filtro divisor.

Todos DirectShow filtros expõem a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e todos os pinos expõem a interface [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) DirectShow também define muitas outras interfaces que suportam funcionalidades mais específicas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de Graph Filtro](about-the-filter-graph-manager.md)
</dt> <dt>

[Dados Flow no filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



