---
description: A classe RealTimeStylus permite que você interaja com o fluxo de dados da caneta eletrônica. Para interagir com o fluxo de dados, adicione um objeto RealTimeStylus ao seu aplicativo e adicione plug-ins ao objeto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Trabalhando com as APIs do StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788890"
---
# <a name="working-with-the-stylusinput-apis"></a>Trabalhando com as APIs do StylusInput

A classe [**RealTimeStylus**](realtimestylus-class.md) permite que você interaja com o fluxo de dados da caneta eletrônica. Para interagir com o fluxo de dados, adicione um objeto **RealTimeStylus** ao seu aplicativo e adicione plug-ins ao objeto **RealTimeStylus** .

Os plug-ins podem modificar os dados associados aos pacotes no ar, à caneta, aos pacotes e aos métodos de notificação de caneta. Os plug-ins podem cancelar os pacotes em ar e os métodos de notificação de pacotes. Os plug-ins também podem adicionar dados de aplicativo ao fluxo na forma de objetos [CustomStylusData](/previous-versions/ms575208(v=vs.100)) . A lista a seguir oferece ideias para categorias comuns de plug-ins que talvez você queira usar ou criar.

-   Plug-in de filtro: um objeto que remove ou cancela seletivamente dados no fluxo de dados da caneta eletrônica.
-   Plug-in do modificador: um objeto que modifica dados seletivamente no fluxo de dados da caneta eletrônica.
-   Plug-in de processador dinâmico: um objeto que exibe os dados da caneta do Tablet em tempo real conforme ele está sendo manipulado pelo objeto [**RealTimeStylus**](realtimestylus-class.md) . Posteriormente, para eventos como uma atualização de formulário, o plug-in de processamento dinâmico ou um plug-in de coleção de tinta pode redesenhar a tinta.
-   Plug-in do reconhecedor: um objeto que examina a movimentação da caneta do Tablet para gestos, manuscritos ou outros glifos.
-   Plug-in do coletor de tinta: um objeto do fluxo de dados da caneta do Tablet cria e armazena a tinta.
-   Plug-in de wrapper: um plug-in que atua como uma interface entre o objeto [**RealTimeStylus**](realtimestylus-class.md) e outro plug-in ou objeto como uma maneira de modificar o comportamento do objeto encapsulado.

Os plug-ins de renderização dinâmica e de coleção de tinta podem ser criados para serem renderizados em vários contextos — como em um arquivo, um fluxo ou em um dispositivo de vídeo. A tinta também pode ser armazenada em vários formatos, como um objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) , um arquivo de Graphics Interchange Format reforçada (GIF), um arquivo ISF (formato serializado de tinta) ou outros formatos.

Dois plug-ins são fornecidos com as APIs StylusInput: a classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e a classe [**GestureRecognizer**](gesturerecognizer-class.md) . A classe **DynamicRenderer** fornece renderização básica dos dados de tinta em tempo real e é simplificada para ter um impacto mínimo no desempenho. A classe **GestureRecognizer** fornece reconhecimento de gesto para a classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="in-this-section"></a>Nesta seção

-   [Trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
-   [Plug-ins de processamento dinâmico](dynamic-renderer-plug-ins.md)
-   [Plug-ins do Recognizer](recognizer-plug-ins.md)

 

 
