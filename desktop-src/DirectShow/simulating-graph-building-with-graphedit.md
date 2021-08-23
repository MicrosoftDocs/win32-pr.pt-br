---
description: Simulando Graph com GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulando Graph com GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4f5bee201e2bd5b771348596b46caa513944aa148c7ec17a9e2974a360e60c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583187"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulando Graph com GraphEdit

DirectShow fornece um utilitário de depuração chamado GraphEdit, que pode ser usado para criar e testar grafos de filtro.

GraphEdit é uma ferramenta visual para criar grafos de filtro. Com o GraphEdit, você pode experimentar um grafo de filtro antes de escrever qualquer código do aplicativo. Você também pode carregar um grafo de filtro que seu aplicativo cria para verificar se o aplicativo está criando o grafo correto. Se você desenvolver um filtro personalizado, o GraphEdit fornece uma maneira rápida de testá-lo: basta carregar um grafo com seu filtro personalizado e tentar executar o grafo. Se você não estiver familiarizado DirectShow, GraphEdit é uma boa maneira de se familiarizar com grafos de filtro e a DirectShow arquitetura.

A ilustração a seguir mostra como GraphEdit representa um grafo de filtro simples.

![grafo de filtro simples em graphedit](images/gedit09.png)

Cada filtro é representado como um retângulo. Quadrados menores ao longo das bordas dos filtros representam pinos. Os pinos de entrada estão no lado esquerdo do filtro e os pinos de saída estão no lado direito. As setas representam as conexões entre pinos.

Com GraphEdit, você pode:

-   Crie e modifique grafos de filtro usando uma interface visual, arrastar e soltar.
-   Simular chamadas programáticas para criar um grafo.
-   Executar, pausar, parar e buscar um grafo.
-   Veja quais filtros estão registrados em seu computador e veja as informações do Registro para cada filtro.
-   Exibir páginas de propriedades de filtro.
-   Exibir os tipos de mídia de conexões de pino.

Esta seção contém os seguintes tópicos:

-   [Usando GraphEdit](using-graphedit.md)
-   [Carregando um Graph de um processo externo](loading-a-graph-from-an-external-process.md)
-   [Salvando um filtro Graph um arquivo GraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Carregando um arquivo GraphEdit programaticamente](loading-a-graphedit-file-programmatically.md)
-   [Formato de arquivo GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow](using-directshow.md)
</dt> </dl>

 

 



