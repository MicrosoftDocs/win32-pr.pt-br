---
description: Simulando a criação de gráficos com o GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulando a criação de gráficos com o GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456686"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulando a criação de gráficos com o GraphEdit

O DirectShow fornece um utilitário de depuração chamado GraphEdit, que pode ser usado para criar e testar grafos de filtro.

GraphEdit é uma ferramenta Visual para criar gráficos de filtro. Com o GraphEdit, você pode experimentar um grafo de filtro antes de escrever qualquer código de aplicativo. Você também pode carregar um grafo de filtro que seu aplicativo cria, para verificar se seu aplicativo está criando o grafo correto. Se você desenvolver um filtro personalizado, o GraphEdit fornecerá uma maneira rápida de testá-lo: basta carregar um grafo com seu filtro personalizado e tentar executar o grafo. Se você for novo no DirectShow, o GraphEdit é uma boa maneira de se familiarizar com grafos de filtro e com a arquitetura do DirectShow.

A ilustração a seguir mostra como GraphEdit representa um gráfico de filtro simples.

![Grafo de filtro simples em GraphEdit](images/gedit09.png)

Cada filtro é representado como um retângulo. Quadrados menores ao longo das bordas dos filtros representam Pins. Os Pins de entrada estão no lado esquerdo do filtro, e os Pins de saída estão no lado direito. As setas representam as conexões entre os Pins.

Com o GraphEdit, você pode:

-   Criar e modificar gráficos de filtro usando uma interface visual, arrastar e soltar.
-   Simular chamadas programáticas para criar um grafo.
-   Executar, pausar, parar e buscar um grafo.
-   Veja quais filtros estão registrados em seu computador e exiba informações de registro para cada filtro.
-   Exibir páginas de propriedades de filtro.
-   Exiba os tipos de mídia de conexões de PIN.

Esta seção contém os seguintes tópicos:

-   [Usando GraphEdit](using-graphedit.md)
-   [Carregando um grafo a partir de um processo externo](loading-a-graph-from-an-external-process.md)
-   [Salvando um grafo de filtro em um arquivo GraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Carregando um arquivo GraphEdit programaticamente](loading-a-graphedit-file-programmatically.md)
-   [Formato de arquivo GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 



