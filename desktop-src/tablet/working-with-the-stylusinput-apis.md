---
description: A classe RealTimeStylus permite que você interaja com o fluxo de dados da caneta do tablet. Para interagir com o fluxo de dados, adicione um objeto RealTimeStylus ao seu aplicativo e adicione plug-ins ao objeto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Trabalhando com as APIs StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143cb885cda16542a65aa096cdf95eb8a187b4f760a916a895887737ec63d7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842836"
---
# <a name="working-with-the-stylusinput-apis"></a>Trabalhando com as APIs StylusInput

A [**classe RealTimeStylus**](realtimestylus-class.md) permite que você interaja com o fluxo de dados da caneta do tablet. Para interagir com o fluxo de dados, adicione um objeto **RealTimeStylus** ao seu aplicativo e adicione plug-ins ao **objeto RealTimeStylus.**

Os plug-ins podem modificar os dados associados aos pacotes in-air, à caneta inocentada, aos pacotes e aos métodos de notificação de up da caneta. Os plug-ins podem cancelar os métodos de notificação de pacotes e pacotes no ar. Os plug-ins também podem adicionar dados do aplicativo ao fluxo na forma de [objetos CustomStylusData.](/previous-versions/ms575208(v=vs.100)) A lista a seguir oferece ideias para categorias comuns de plug-ins que talvez você queira usar ou criar.

-   Plug-in de filtro: um objeto que remove ou cancela dados seletivamente no fluxo de dados da caneta tablet.
-   Plug-in modificador: um objeto que modifica seletivamente os dados no fluxo de dados da caneta tablet.
-   Plug-in do renderador dinâmico: um objeto que exibe os dados da caneta de tablet em tempo real enquanto eles estão sendo manipulados pelo [**objeto RealTimeStylus.**](realtimestylus-class.md) Posteriormente, para eventos como uma atualização de formulário, o plug-in do renderador dinâmico ou um plug-in de coleção de tinta podem redesenhar a tinta.
-   Plug-in do Reconhecedor: um objeto que examina o movimento da caneta de tablet em busca de gestos, manuscrito ou outros glifos.
-   Plug-in do coletor de tinta: um objeto que do fluxo de dados da caneta de tablet cria e armazena tinta.
-   Plug-in wrapper: um plug-in que atua como uma interface entre o objeto [**RealTimeStylus**](realtimestylus-class.md) e outro plug-in ou objeto como uma maneira de modificar o comportamento do objeto empacotado.

Os plug-ins de renderização dinâmica e de coleção de tinta podem ser criados para renderizar para vários contextos, como para um arquivo, um fluxo ou para um dispositivo de exibição. A tinta também pode ser armazenada em vários formatos, como um objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) um arquivo GIF (Graphics Interchange Format), um arquivo ISF (formato ISF) ou outros formatos.

Dois plug-ins são fornecidos com as APIs StylusInput: a [**classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e a [**classe GestureRecognizer.**](gesturerecognizer-class.md) A **classe DynamicRenderer** fornece renderização básica dos dados de tinta em tempo real e é simplificada para ter um impacto mínimo no desempenho. A **classe GestureRecognizer** fornece reconhecimento de gesto para a [**classe RealTimeStylus.**](realtimestylus-class.md)

## <a name="in-this-section"></a>Nesta seção

-   [Trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
-   [Plug-ins de renderização dinâmica](dynamic-renderer-plug-ins.md)
-   [Plug-ins do Reconhecedor](recognizer-plug-ins.md)

 

 
