---
title: Definindo tarefas e opcodes
description: Os provedores usam tarefas e opcodes para agrupar eventos logicamente. O agrupamento de eventos ajuda os consumidores a consultar apenas os eventos que contêm combinações específicas de tarefa e opcode.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb576251edf4de14c564c6e468209ece93e5840da9e0d821c20b132794f48ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032466"
---
# <a name="defining-tasks-and-opcodes"></a>Definindo tarefas e opcodes

Os provedores usam tarefas e opcodes para agrupar eventos logicamente. O agrupamento de eventos ajuda os consumidores a consultar apenas os eventos que contêm combinações específicas de tarefa e opcode. Normalmente, você usa tarefas para identificar um componente principal do provedor, como o componente de rede ou de banco de dados. Em seguida, você pode usar opcodes para identificar as operações que o componente executa, como as operações de envio e recebimento para um componente de rede. Se você tivesse apenas um componente, poderia usar a tarefa para refletir uma grande operação no componente, como conectar ou desconectar e usar opcode para refletir uma atividade dentro da operação, como ler o registro. Você também pode usar o opcode sem especificar uma tarefa. A maneira como você usa a tarefa e os opcodes para agrupar eventos para o consumidor é completamente seu.

Para definir uma tarefa, use o elemento **Task** . Para definir um opcode, use o elemento **opcode** . Você pode especificar até 228 OpCodes. O **valor** da tarefa deve ser maior que 0. Os opcodes devem estar no intervalo de 11 a 239. O arquivo de Winmeta.xml define operações comuns que você pode usar em vez de definir as suas próprias.

O exemplo a seguir mostra como definir várias tarefas e OpCodes.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
