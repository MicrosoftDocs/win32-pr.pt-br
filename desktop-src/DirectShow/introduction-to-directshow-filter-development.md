---
description: Introdução ao desenvolvimento de filtro do DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introdução ao desenvolvimento de filtro do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105788081"
---
# <a name="introduction-to-directshow-filter-development"></a>Introdução ao desenvolvimento de filtro do DirectShow

Esta seção fornece uma breve descrição das tarefas envolvidas no desenvolvimento de um filtro do DirectShow personalizado. Ele também fornece links para tópicos que discutem essas tarefas com mais detalhes. Antes de ler esta seção, leia os tópicos em [sobre o DirectShow](about-directshow.md), que descrevem a arquitetura geral do DirectShow.

**Biblioteca de classes base do DirectShow**

O SDK do DirectShow inclui um conjunto de classes C++ para a gravação de filtros. Embora não sejam necessárias, essas classes são a maneira recomendada para escrever um novo filtro. Para usar as classes base, compile-as em uma biblioteca estática e vincule o arquivo. lib ao seu projeto, conforme descrito em [Criando filtros do DirectShow](building-directshow-filters.md).

A biblioteca de classes base define uma classe raiz para filtros, a classe [**CBaseFilter**](cbasefilter.md) . Várias outras classes derivam de **CBaseFilter** e são especializadas para determinados tipos de filtros. Por exemplo, a classe [**CTransformFilter**](ctransformfilter.md) foi projetada para filtros de transformação. Para criar um novo filtro, implemente uma classe que herde de uma das classes de filtro. Por exemplo, sua declaração de classe pode ser da seguinte maneira:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Para obter mais informações sobre as classes base do DirectShow, consulte os seguintes tópicos:

-   [Classes base do DirectShow](directshow-base-classes.md)
-   [Criando filtros do DirectShow](building-directshow-filters.md)

**Criando Pins**

Um filtro deve criar um ou mais Pins. O número de Pins pode ser corrigido no tempo de design ou o filtro pode criar novos PINs, conforme necessário. Os Pins geralmente derivam da classe [**CBasePin**](cbasepin.md) ou de uma classe que herda **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md). Os Pins do filtro devem ser declarados como variáveis de membro na classe de filtro. Algumas das classes de filtro já definem os Pins, mas se o filtro herdar diretamente do **CBaseFilter**, você deverá declarar os Pins em sua classe derivada.

**Negociando conexões de PIN**

Quando o Gerenciador de gráficos de filtro tenta conectar dois filtros, os Pins devem concordar com várias coisas. Se não puderem, a tentativa de conexão falhará. Em geral, os Pins negociam o seguinte:

-   Transport: O transporte é o mecanismo que os filtros usarão para mover amostras de mídia do pino de saída para o pino de entrada. Por exemplo, eles podem usar a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo de push") ou a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de pull").
-   Tipo de mídia. Quase todos os Pins usam tipos de mídia para descrever o formato dos dados que eles fornecerão.
-   Alocador. O alocador é o objeto que cria os buffers que contêm os dados. Os Pins devem concordar com qual PIN fornecerá o alocador. Eles também devem concordar com o tamanho dos buffers, o número de buffers a serem criados e outras propriedades de buffer.

As classes base implementam uma estrutura para essas negociações. Você deve concluir os detalhes substituindo vários métodos na classe base. O conjunto de métodos que você deve substituir depende da classe e da funcionalidade do seu filtro. Para obter mais informações, consulte [como os filtros se conectam](how-filters-connect.md).

**Processando e entregando dados**

A função principal da maioria dos filtros é processar e entregar dados de mídia. Como isso ocorre depende do tipo de filtro:

-   Uma fonte Push tem um thread de trabalho que preenche continuamente os exemplos com os dados e os entrega.
-   Uma fonte de pull espera por seu vizinho downstream para solicitar um exemplo. Ele responde gravando dados em um exemplo e entregando o exemplo ao filtro downstream. O filtro downstream cria o thread que orienta o fluxo de dados.
-   Um filtro de transformação tem exemplos entregues a ele pelo vizinho upstream. Quando recebe um exemplo, ele processa os dados e os entrega por downstream.
-   Um filtro de renderizador recebe amostras de upstream e os agenda para renderização com base nos carimbos de data/hora.

Outras tarefas relacionadas ao streaming incluem a liberação de dados do grafo, o tratamento do fim do fluxo e a resposta a solicitações de busca. Para obter mais informações sobre esses problemas, consulte os seguintes tópicos:

-   [Fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md)
-   [Gerenciamento de controle de qualidade](quality-control-management.md)
-   [Threads e seções críticas](threads-and-critical-sections.md)

**COM suporte a**

Os filtros do DirectShow são objetos COM, normalmente empacotados em DLLs. A biblioteca de classes base implementa uma estrutura para dar suporte a COM. Ele é descrito na seção [DirectShow e com](directshow-and-com.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



