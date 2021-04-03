---
description: 'Quando a função SetupCommitFileQueue confirma a fila de arquivos, ela processa as operações de arquivo na seguinte ordem: operações de exclusão de arquivo, operações de renomeação de arquivo e, por fim, operações de cópia de arquivo.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordem de compromisso de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828688"
---
# <a name="order-of-queue-commitment"></a>Ordem de compromisso de fila

Quando a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirma a fila de arquivos, ela processa as operações de arquivo na seguinte ordem: operações de exclusão de arquivo, operações de renomeação de arquivo e, por fim, operações de cópia de arquivo. A estrutura de tópicos a seguir ilustra o ciclo de vida do processo de compromisso de uma fila.

 

-   iniciar a exclusão da subfila
    -   iniciar uma operação de exclusão de arquivo <--repetir para cada
    -   concluir uma operação de exclusão de arquivo <--exclusão de arquivo na fila
-   concluir a exclusão da subfila

<!-- -->

-   iniciar a subfila de renomeação
    -   iniciar uma operação de renomeação de arquivo <--repetir para cada
    -   concluir uma operação de exclusão de arquivo <--renomeação de arquivo na fila
-   concluir a subfila de renomeação

<!-- -->

-   Inicie a cópia subque
    -   iniciar uma operação de cópia de arquivo <--repetir para cada
    -   concluir uma operação de cópia de arquivo <--cópia de arquivo na fila
    -   concluir a cópia da subfila
-   concluir a fila

 

Em cada etapa, ou se ocorrer um erro, a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviará uma notificação para a rotina de retorno de chamada. A rotina de retorno de chamada pode usar as informações enviadas pela fila para acompanhar o progresso da instalação e, se necessário, interagir com o usuário.

Por exemplo, se uma operação de cópia de arquivo precisar de um arquivo de origem que não estava disponível no caminho atual, o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviará uma notificação de SPFILENOTIFY \_ NEEDMEDIA para a rotina de retorno de chamada, juntamente com informações sobre o arquivo e a mídia necessária. A rotina de retorno de chamada pode usar essas informações para gerar uma caixa de diálogo que solicita ao usuário para inserir o próximo disco chamando [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Uma rotina de retorno de chamada de fila padrão, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), está incluída na API de instalação. Essa rotina manipula notificações de fila e gera caixas de diálogo de erro e barras de progresso para a instalação. Você pode usar a rotina de retorno de chamada de fila padrão como está, ou escrever uma rotina de retorno de chamada de filtro para manipular um subconjunto das notificações e passar os outros para a rotina de retorno de chamada de fila padrão.

Se nenhuma das funcionalidades da rotina de retorno de chamada atender às suas necessidades, você poderá escrever uma rotina de retorno de chamada personalizada independente que não chame a rotina de retorno de chamada de fila padrão.

Para obter mais informações sobre rotinas de retorno de chamada de fila, consulte [rotina de retorno de chamada de fila padrão](default-queue-callback-routine.md)e [criando uma rotina de retorno de chamada de fila personalizada](creating-a-custom-queue-callback-routine.md)

 

 



