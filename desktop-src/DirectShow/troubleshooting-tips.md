---
description: Dicas de solução de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Dicas de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fe361af291c29f8784235066f341d940ab38205cd3b8238896011f85021a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651238"
---
# <a name="troubleshooting-tips"></a>Dicas de solução de problemas

as dicas a seguir ajudarão você a evitar deadlocks ou falhas no seu aplicativo DirectShow.

**Objetos globais**

um objeto C++ global não deve criar DirectShow objetos em seu método construtor ou liberá-los em seu método destruidor. Isso pode fazer com que o aplicativo seja bloqueado indefinidamente, pelo seguinte motivo:

Não é possível sair de threads enquanto estiver dentro da função de ponto de entrada de uma DLL. O kernel 32 mantém um bloqueio de processo global durante a função de ponto de entrada e o bloqueio impede que o thread seja encerrado. como alguns DirectShow objetos próprios threads, eles podem bloquear se forem liberados de dentro de uma função de ponto de entrada de DLL. Se um aplicativo tiver um objeto C++ global, a DLL de tempo de execução C chamará o destruidor do objeto quando a DLL for descarregada. se o destruidor liberar DirectShow objetos, ele poderá bloquear como resultado.

por motivos semelhantes, uma DLL não deve criar ou liberar DirectShow objetos em sua rotina de ponto de entrada.

**Liberando interfaces**

você deve liberar todos os ponteiros de interface DirectShow enquanto seu aplicativo ainda está processando mensagens, antes de sair do loop de mensagem. caso contrário, você poderá ver várias declarações, porque alguns DirectShow objetos enviam mensagens durante suas rotinas de limpeza.

(Como um registro, se você estiver usando a classe **CWindowImpl** do ATL, não espere até que **OnFinalMessage** libere as interfaces. Em vez disso, libere-os quando você manipular a mensagem de fechamento do WM \_ .)

**Contagens de referência**

quando a versão de depuração do Quartz.dll descarrega, ela verifica se algum DirectShow objetos têm contagens de referência que não foram lançadas. Nesse caso, ele gera uma asserção:


```C++
g_cFGObjects == 0 
```



Quando essa asserção falha, significa que seu aplicativo perdeu uma contagem de referência. Examine seu código e certifique-se de liberar todos os ponteiros de interface.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depurando no DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



