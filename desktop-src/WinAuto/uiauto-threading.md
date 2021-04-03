---
title: Noções básicas sobre problemas de Threading
description: Este tópico descreve cenários de Threading comuns para implementações do cliente de automação da interface do usuário da Microsoft e explica como evitar problemas que podem ocorrer se um cliente usa o Threading incorretamente.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clientes, problemas de threading de automação da interface do usuário
- clientes, problemas de Threading
- clientes, modelo de Threading do manipulador de eventos
- clientes, modelo de Threading do manipulador de eventos de automação da interface do usuário
- clientes, afinidade de automação da interface do usuário
- clientes, afinidade
- Automação da interface do usuário, problemas de Threading
- Automação da interface do usuário, modelo de Threading do manipulador de eventos
- Automação da interface do usuário, afinidade
- problemas com threading
- modelo de Threading do manipulador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007601"
---
# <a name="understanding-threading-issues"></a>Noções básicas sobre problemas de Threading

Este tópico descreve cenários de Threading comuns para implementações do cliente de automação da interface do usuário da Microsoft e explica como evitar problemas que podem ocorrer se um cliente usa o Threading incorretamente.

Este tópico contém as seguintes seções:

-   [Automação da interface do usuário e thread da interface do usuário](#ui-automation-and-the-ui-thread)
-   [Modelo de threading para manipuladores de eventos](#threading-model-for-event-handlers)
-   [Afinidade de apartamento COM em Windows de 64 bits](#com-apartment-affinity-on-64-bit-windows)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Automação da interface do usuário e thread da interface do usuário

Devido à maneira como a automação da interface do usuário usa mensagens do Windows, os conflitos podem ocorrer quando um aplicativo cliente tenta interagir com sua própria interface do usuário no thread da interface do usuário. Esses conflitos podem levar a um desempenho muito lento ou até mesmo fazer com que o aplicativo pare de responder.

Se o seu aplicativo cliente se destina a interagir com todos os elementos na área de trabalho, incluindo sua própria interface do usuário, você deve fazer todas as chamadas de automação da interface do usuário de um thread separado. Isso inclui a localização de elementos, por exemplo, usando [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) ou o método [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) e o uso de padrões de controle. Esse thread não deve possuir nenhuma janela e deve ser um thread de modelo MTA (multithreaded apartment) Component Object Model (COM) (um que inicializa o COM chamando [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador **coinit \_ multi-threaded** .)

É seguro fazer chamadas de automação da interface do usuário em um manipulador de eventos de automação da interface do usuário, pois o manipulador de eventos é sempre chamado em um thread que não seja da interface do usuário. No entanto, ao assinar eventos que podem se originar da interface do usuário do aplicativo cliente, você deve fazer a chamada para [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)ou um método relacionado, em um thread que não seja de interface do usuário (que também deve ser um thread MTA). Remova os manipuladores de eventos no mesmo thread.

Um cliente de automação de interface do usuário não deve usar vários threads para adicionar ou remover manipuladores de eventos. Um comportamento inesperado pode ocorrer se um manipulador de eventos estiver sendo adicionado ou removido enquanto outro estiver sendo adicionado ou removido no mesmo processo de cliente.

## <a name="threading-model-for-event-handlers"></a>Modelo de threading para manipuladores de eventos

Um cliente de automação de interface do usuário deve usar o modelo de Threading do MTA COM para threads que implementam manipuladores de eventos. O uso do modelo STA (single-threaded apartment) pode causar problemas como, por exemplo, impedir que os clientes removam manipuladores de eventos do thread.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>Afinidade de apartamento COM em Windows de 64 bits

De acordo com a especificação COM, o tempo de vida de um objeto remoto é regido pelo tempo de vida do apartamento em que a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é chamada para criar o objeto. Quando o apartamento original é desligado, o objeto remoto também é liberado.

Para clientes de automação da interface do usuário, esse comportamento de COM pode significar que o tempo de vida do auxiliar remoto 32/64 (criado por UIAutomationCore.dll) usado por um elemento de 32 bits é regido pelo tempo de vida do apartamento do thread que criou o elemento. Se o cliente de automação da interface do usuário realizar marshaling do elemento para outro thread, o elemento poderá se tornar invalidado quando o apartamento de origem for desligado. O cliente de automação da interface do usuário deve lidar com esses problemas normalmente Capturando erros ao usar elementos de automação empacotados.

O mesmo problema pode ocorrer com um cliente de automação de interface do usuário de 32 bits que tem elementos de 64 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> <dt>

[Inscrevendo-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[INFORMAÇÕES: descrições e trabalho de modelos de Threading OLE](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 