---
description: Dicas de solução de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Dicas de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770427"
---
# <a name="troubleshooting-tips"></a>Dicas de solução de problemas

Estas dicas a seguir ajudarão você a evitar deadlocks ou falhas em seu aplicativo do DirectShow.

**Objetos globais**

Um objeto C++ global não deve criar objetos DirectShow em seu método construtor ou liberá-los em seu método destruidor. Isso pode fazer com que o aplicativo seja bloqueado indefinidamente, pelo seguinte motivo:

Não é possível sair de threads enquanto estiver dentro da função de ponto de entrada de uma DLL. O kernel 32 mantém um bloqueio de processo global durante a função de ponto de entrada e o bloqueio impede que o thread seja encerrado. Como alguns objetos do DirectShow possuem threads, eles podem ser bloqueados se forem liberados de dentro de uma função de ponto de entrada de DLL. Se um aplicativo tiver um objeto C++ global, a DLL de tempo de execução C chamará o destruidor do objeto quando a DLL for descarregada. Se o destruidor liberar objetos do DirectShow, ele poderá bloquear como resultado.

Por motivos semelhantes, uma DLL não deve criar ou liberar objetos do DirectShow em sua rotina de ponto de entrada.

**Liberando interfaces**

Você deve liberar todos os ponteiros de interface do DirectShow enquanto seu aplicativo ainda estiver processando mensagens, antes de sair do loop de mensagem. Caso contrário, você poderá ver várias declarações, pois alguns objetos do DirectShow enviam mensagens durante suas rotinas de limpeza.

(Como um registro, se você estiver usando a classe **CWindowImpl** do ATL, não espere até que **OnFinalMessage** libere as interfaces. Em vez disso, libere-os quando você manipular a mensagem de fechamento do WM \_ .)

**Contagens de referência**

Quando a versão de depuração do Quartz.dll descarrega, ela verifica se algum objeto do DirectShow tem contagens de referência que não foram lançadas. Nesse caso, ele gera uma asserção:


```C++
g_cFGObjects == 0 
```



Quando essa asserção falha, significa que seu aplicativo perdeu uma contagem de referência. Examine seu código e certifique-se de liberar todos os ponteiros de interface.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depuração no DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



