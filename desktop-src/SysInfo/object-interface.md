---
description: 'O Windows fornece funções que executam as seguintes tarefas:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interface de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461191"
---
# <a name="object-interface"></a>Interface de objeto

O Windows fornece funções que executam as seguintes tarefas:

-   Criar um objeto
-   Obter um identificador de objeto
-   Obter informações sobre o objeto
-   Definir informações sobre o objeto
-   Fechar o identificador de objeto
-   Destruir o objeto

Algumas dessas tarefas não são necessárias para cada objeto. Algumas dessas tarefas são combinadas para determinados objetos. Por exemplo, um aplicativo pode criar um objeto de evento. Outros aplicativos podem abrir o evento para obter um identificador exclusivo para esse objeto de evento. À medida que cada aplicativo termina de usar o evento, ele fecha seu identificador para o objeto. Quando não há identificadores abertos restantes para o objeto de evento, o sistema destrói o objeto de evento. Por outro lado, um aplicativo pode obter um identificador para um objeto de janela existente. Quando o objeto Window não é mais necessário, o aplicativo deve destruir o objeto, o que invalida o identificador de janela.

Ocasionalmente, um objeto permanece na memória depois que todos os identificadores de objeto foram fechados. Por exemplo, um thread pode criar um objeto de evento e aguardar o identificador de evento. Enquanto o thread está aguardando, outro thread pode fechar o mesmo identificador de objeto de evento. O objeto de evento permanece na memória, sem identificadores de objeto de evento, até que o objeto de evento seja definido como o estado sinalizado e a operação de espera seja concluída. Neste momento, o sistema remove o objeto da memória.

Identificadores e objetos consomem memória. Portanto, para preservar o desempenho do sistema, você deve fechar identificadores e excluir objetos assim que eles não forem mais necessários. Se você não fizer isso, seu aplicativo poderá prejudicar o desempenho do sistema, devido ao uso excessivo do arquivo de paginação.

Quando um processo é encerrado, o sistema fecha automaticamente os identificadores e exclui os objetos criados pelo processo. No entanto, quando um thread é encerrado, o sistema geralmente não fecha identificadores ou exclui objetos. As únicas exceções são janela, gancho, posição da janela e objetos de conversa DDE (troca de dados dinâmicos); esses objetos são destruídos quando o thread de criação é encerrado.

 

 



