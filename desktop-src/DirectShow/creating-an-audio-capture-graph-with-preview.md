---
description: Criando um grafo de captura de áudio com visualização
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Criando um grafo de captura de áudio com visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920085"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a>Criando um grafo de captura de áudio com visualização

O gráfico de filtro descrito em [criando um grafo de captura de áudio](creating-an-audio-capture-graph.md) executa somente a captura, sem visualização. Para visualizar e capturar ao mesmo tempo, o grafo de filtro precisa usar o [filtro de t de PIN infinito](infinite-pin-tee-filter.md). Esse filtro tem um PIN de entrada e cria quantos Pins de saída forem necessários. (Começa com um pino de saída. Cada vez que você conecta um PIN de saída, ele cria outro.) O filtro de baixo do PIN infinito entrega cada exemplo que recebe, inalterado, por todos os seus PINs de saída.

Conecte o filtro de captura de áudio ao "t" de PIN infinito e conecte o "t" de PIN infinito ao Multiplexador e ao [filtro de renderizador DirectSound](directsound-renderer-filter.md). Conecte o multiplexador ao gravador de arquivos, como antes. O diagrama a seguir ilustra o grafo de filtro resultante para um arquivo AVI.

![Grafo de captura de áudio com visualização](images/audio-capture-graph.png)

Como o renderizador do DirectSound é o processador de áudio padrão, você pode simplesmente chamar o método [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) no pino de saída de t de PIN infinito. O Gerenciador de gráficos de filtro usa a [conexão inteligente](intelligent-connect.md) para criar o renderizador, adicioná-lo ao grafo de filtro e conectar os Pins.

> [!Note]  
> Se você capturar áudio de um microfone e visualizá-lo de um palestrante no mesmo computador, poderá criar comentários de áudio.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 



