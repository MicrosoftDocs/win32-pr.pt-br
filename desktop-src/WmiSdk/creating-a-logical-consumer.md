---
description: Um consumidor lógico é uma instância de uma classe de consumidor de evento permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Criando um consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788758"
---
# <a name="creating-a-logical-consumer"></a>Criando um consumidor lógico

Um consumidor lógico é uma instância de uma classe de consumidor de evento permanente. A principal finalidade de um consumidor lógico é fornecer ao consumidor físico os parâmetros para as atividades que o consumidor físico realiza. Para obter mais informações, consulte [criando uma nova classe de consumidor de evento permanente](creating-a-new-permanent-event-consumer-class.md). O consumidor permanente deve ter o mesmo [**CreatorSID**](--eventconsumer.md) nas instâncias de consumidor, filtro e associação. Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md). Para obter um exemplo de como usar um consumidor lógico, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md), que mostra o uso da classe de consumidor padrão [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para configurar um consumidor permanente.

O procedimento a seguir descreve como criar um consumidor lógico.

**Para criar um consumidor lógico**

1.  Crie uma instância de sua classe de consumidor permanente.
2.  Preencha as propriedades da instância com os parâmetros da ação que você deseja que o consumidor físico execute.

O exemplo de código MOF a seguir descreve um consumidor lógico que contém um script.

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Depois de criar o consumidor lógico, você deve vincular cada filtro a um filtro de eventos para atribuir a ação a um evento específico. Para obter mais informações, consulte [criando um filtro de eventos](creating-an-event-filter.md).

 

 



