---
description: Introdução ao desenvolvimento DirectShow filtro
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introdução ao desenvolvimento DirectShow filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083686"
---
# <a name="introduction-to-directshow-filter-development"></a>Introdução ao desenvolvimento DirectShow filtro

Esta seção fornece uma breve delineia das tarefas envolvidas no desenvolvimento de um filtro DirectShow personalizado. Ele também fornece links para tópicos que discutem essas tarefas com mais detalhes. Antes de ler esta seção, leia os tópicos em [Sobre DirectShow](about-directshow.md), que descrevem a arquitetura DirectShow geral.

**DirectShow Biblioteca de Classes Base**

O DirectShow SDK inclui um conjunto de classes C++ para escrever filtros. Embora não sejam necessárias, essas classes são a maneira recomendada de escrever um novo filtro. Para usar as classes base, compile-as em uma biblioteca estática e vincule o arquivo .lib ao seu projeto, conforme descrito em Criando [filtros DirectShow .](building-directshow-filters.md)

A biblioteca de classes base define uma classe raiz para filtros, a [**classe CBaseFilter.**](cbasefilter.md) Várias outras classes derivam **de CBaseFilter** e são especializadas para tipos específicos de filtros. Por exemplo, a [**classe CTransformFilter**](ctransformfilter.md) foi projetada para filtros de transformação. Para criar um novo filtro, implemente uma classe que herda de uma das classes de filtro. Por exemplo, sua declaração de classe pode ser a seguinte:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Para obter mais informações sobre as DirectShow base, consulte os seguintes tópicos:

-   [DirectShow Base Classes](directshow-base-classes.md)
-   [Criando filtros DirectShow dados](building-directshow-filters.md)

**Criando pinos**

Um filtro deve criar um ou mais pinos. O número de pinos pode ser corrigido em tempo de design ou o filtro pode criar novos pinos conforme necessário. Os pinos geralmente derivam da [**classe CBasePin**](cbasepin.md) ou de uma classe que herda **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md). Os pinos do filtro devem ser declarados como variáveis de membro na classe de filtro. Algumas das classes de filtro já definem os pinos, mas se o filtro herda diretamente de **CBaseFilter**, você deve declarar os pinos em sua classe derivada.

**Negociando conexões de pino**

Quando o Gerenciador Graph Filtro tenta conectar dois filtros, os pinos devem concordar com várias coisas. Se não puderem, a tentativa de conexão falhará. Em geral, os pinos negociam o seguinte:

-   Transport: O transporte é o mecanismo que os filtros usarão para mover amostras de mídia do pino de saída para o pino de entrada. Por exemplo, eles podem usar a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo push") ou a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de pull").
-   Tipo de mídia. Quase todos os pinos usam tipos de mídia para descrever o formato dos dados que eles fornecerão.
-   Alocador. O alocador é o objeto que cria os buffers que mantém os dados. Os pinos devem concordar com qual pino fornecerá o alocador. Eles também devem concordar com o tamanho dos buffers, o número de buffers a criar e outras propriedades de buffer.

As classes base implementam uma estrutura para essas negociações. Você deve concluir os detalhes substituindo vários métodos na classe base. O conjunto de métodos que você deve substituir depende da classe e da funcionalidade do filtro. Para obter mais informações, consulte [Como filtros Conexão](how-filters-connect.md).

**Processamento e entrega de dados**

A função principal da maioria dos filtros é processar e fornecer dados de mídia. Como isso ocorre depende do tipo de filtro:

-   Uma fonte de push tem um thread de trabalho que preenche continuamente amostras com dados e as entrega downstream.
-   Uma fonte de pull aguarda seu vizinho downstream solicitar um exemplo. Ele responde escrevendo dados em um exemplo e entregando o exemplo para o filtro downstream. O filtro downstream cria o thread que orienta o fluxo de dados.
-   Um filtro de transformação tem amostras entregues a ele por seu vizinho upstream. Quando recebe um exemplo, ele processa os dados e os entrega downstream.
-   Um filtro do renderador recebe exemplos de upstream e agenda-os para renderização com base nos carimbos de data/hora.

Outras tarefas relacionadas ao streaming incluem a liberação de dados do grafo, o tratamento do final do fluxo e a resposta às solicitações de busca. Para obter mais informações sobre esses problemas, consulte os seguintes tópicos:

-   [Dados Flow para desenvolvedores de filtro](data-flow-for-filter-developers.md)
-   [Gerenciamento de controle de qualidade](quality-control-management.md)
-   [Threads e seções críticas](threads-and-critical-sections.md)

**Com suporte**

DirectShow filtros são objetos COM, normalmente empacotados em DLLs. A biblioteca de classes base implementa uma estrutura para dar suporte a COM. Ele é descrito na seção DirectShow [e COM](directshow-and-com.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



