---
description: Antes que a rotina de retorno de chamada de fila padrão possa ser usada, especificando-a como a rotina de retorno de chamada ao confirmar uma fila de arquivos ou chamando-a de uma rotina de retorno de chamada personalizada, ela deve ser inicializada.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Inicializando e encerrando o contexto de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67df0707f91a17369503fa17ecbeefef3eb6827be60285b0b778b07d98eba3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965429"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Inicializando e encerrando o contexto de retorno de chamada

Antes que a rotina de retorno de chamada de fila padrão possa ser usada, especificando-a como a rotina de retorno de chamada ao confirmar uma fila de arquivos ou chamando-a de uma rotina de retorno de chamada personalizada, ela deve ser inicializada.

A função [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) cria a estrutura de contexto que é usada pela rotina de retorno de chamada de fila padrão. Ele retorna um ponteiro void para essa estrutura. Essa estrutura é essencial para a operação da rotina de retorno de chamada padrão e deve ser passada para a rotina de retorno de chamada. Isso pode ser feito especificando o ponteiro void como o contexto em uma chamada para [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)ou especificando o ponteiro void como o parâmetro de contexto ao chamar [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) de uma rotina de retorno de chamada personalizada. Essa estrutura de contexto não deve ser alterada ou referenciada pelo aplicativo de instalação.

A função [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) também Inicializa um contexto para a rotina de retorno de chamada de fila padrão, mas especifica uma segunda janela para receber uma mensagem de progresso especificada pelo chamador sempre que a fila envia uma notificação. Isso permite que você use as caixas de diálogo de prompt e erro de disco padrão e também incorpore uma barra de progresso em uma segunda janela, por exemplo, em uma página de um assistente de instalação.

Independentemente de você ter inicializado o contexto usado pela rotina de retorno de chamada de fila padrão com [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), depois que as operações em fila tiverem terminado o processamento, chame [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) para liberar os recursos alocados na inicialização da estrutura de contexto.

 

 



