---
description: Um consumidor lógico é uma instância de uma classe de consumidor de evento permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Criando um consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9514ce3f1c7982a96692dcdea62ec9bb92ebf99dd4c47cfe1a64b70257dcfc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030656"
---
# <a name="creating-a-logical-consumer"></a>Criando um consumidor lógico

Um consumidor lógico é uma instância de uma classe de consumidor de evento permanente. A principal finalidade de um consumidor lógico é fornecer ao consumidor físico os parâmetros para as atividades que o consumidor físico executa. Para obter mais informações, consulte [Criando uma nova classe de consumidor de evento permanente](creating-a-new-permanent-event-consumer-class.md). O consumidor permanente deve ter o mesmo [**CreatorSID**](--eventconsumer.md) nas instâncias de consumidor, filtro e associação. Para obter mais informações, consulte [Recebendo eventos com segurança.](receiving-events-securely.md) Para ver um exemplo de como usar um consumidor lógico, consulte Executando um [script](running-a-script-based-on-an-event.md)baseado em um evento , que mostra o uso da classe de consumidor [**padrão ActiveScriptEventConsumer**](activescripteventconsumer.md) para configurar um consumidor permanente.

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

Depois de criar o consumidor lógico, você deve vincular cada filtro a um filtro de evento para atribuir a ação a um evento específico. Para obter mais informações, consulte [Criando um filtro de evento](creating-an-event-filter.md).

 

 



