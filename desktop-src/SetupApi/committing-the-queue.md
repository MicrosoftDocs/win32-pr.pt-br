---
description: Se a função de retorno de chamada padrão for chamada durante o compromisso da fila, o contexto para ela deverá ser inicializado usando as funções SetupInitDefaultQueueCallback ou SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmação da fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887517"
---
# <a name="committing-the-queue"></a>Confirmação da fila

Se a função de retorno de chamada padrão for chamada durante o compromisso da fila, o contexto para ela deverá ser inicializado usando as funções [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) Se você estiver usando uma função de retorno de chamada personalizada que nunca chama a função de retorno de chamada padrão, essa etapa não será necessária.

Depois que a fila for criada e a função de retorno de chamada que processará notificações de fila tiver sido inicializada, você poderá chamar [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para fazer commit das operações que foram enfileiradas.

O exemplo a seguir [**usa SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para fazer commit da fila usando a rotina de retorno de chamada padrão.

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

No exemplo anterior, MyQueue é a fila a ser confirmada, OwnerWindow é a janela que terá todas as caixas de diálogo criadas pela rotina de retorno de chamada padrão, SetupDefaultQueueCallback especifica que a função de retorno de chamada padrão será usada e *Context* é um ponteiro para a estrutura retornada pela chamada anterior para [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



