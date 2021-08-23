---
description: Operações sobrepostas permitem que um thread execute uma operação de e/s demorada em segundo plano, deixando o thread livre para executar outras tarefas.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Operações sobrepostas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ba148d0b2085e2c44e71c4c8d309f9a068223eebe8de8e239f13095c8ddd39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956885"
---
# <a name="overlapped-operations"></a>Operações sobrepostas

Operações sobrepostas permitem que um thread execute uma operação de e/s demorada em segundo plano, deixando o thread livre para executar outras tarefas. Para habilitar operações de e/s sobrepostas em um recurso de comunicação, o thread deve especificar o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** na função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) quando o identificador é aberto. Para executar a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) como uma operação sobreposta, o thread de chamada deve especificar um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . A estrutura **sobreposta** deve conter um identificador para um objeto de evento de redefinição manual (não é um reinício automático). O sistema define o estado do objeto de evento como não-sinalizado quando uma chamada para a função de e/s retorna antes de a operação ser concluída. O sistema define o estado do objeto de evento para sinalizado quando a operação foi concluída. O thread usa uma função Wait para verificar o estado atual do objeto de evento ou aguardar que seu estado seja sinalizado.

As funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) podem ser executadas somente como operações sobrepostas. O thread de chamada especifica um ponteiro para a função [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , que é executada quando a operação sobreposta é concluída. A rotina de conclusão será executada somente se o thread de chamada executar uma operação de alerta.

Para obter mais informações sobre objetos de evento, funções de espera, esperas de alerta e rotinas de conclusão, consulte [sobre sincronização](/windows/desktop/Sync/about-synchronization).

 

 
