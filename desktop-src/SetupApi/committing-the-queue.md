---
description: Se a função de retorno de chamada padrão for chamada durante o compromisso de fila, o contexto para ela deverá ser inicializado usando as funções SetupInitDefaultQueueCallback ou SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmando a fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753711"
---
# <a name="committing-the-queue"></a>Confirmando a fila

Se a função de retorno de chamada padrão for chamada durante o compromisso de fila, o contexto para ela deverá ser inicializado usando as funções [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) . Se você estiver usando uma função de retorno de chamada personalizada que nunca chama a função de retorno de chamada padrão, essa etapa não será necessária.

Depois que a fila é criada e a função de retorno de chamada que processará as notificações de fila foi inicializada, você pode chamar [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar as operações que foram enfileiradas.

O exemplo a seguir usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar a fila usando a rotina de retorno de chamada padrão.

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

No exemplo anterior, MyQueue é a fila a ser confirmada, OwnerWindow é a janela que terá qualquer caixa de diálogo criada pela rotina de retorno de chamada padrão, SetupDefaultQueueCallback especifica que a função de retorno de chamada padrão será usada e o *contexto* é um ponteiro para a estrutura retornada pela chamada anterior para [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



