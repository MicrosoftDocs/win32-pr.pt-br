---
title: Definindo tarefas e opcodes
description: Os provedores usam tarefas e opcodes para agrupar eventos logicamente. O agrupamento de eventos ajuda os consumidores a consultar apenas os eventos que contêm combinações específicas de tarefa e opcode.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104499011"
---
# <a name="defining-tasks-and-opcodes"></a><span data-ttu-id="be4e7-104">Definindo tarefas e opcodes</span><span class="sxs-lookup"><span data-stu-id="be4e7-104">Defining Tasks and Opcodes</span></span>

<span data-ttu-id="be4e7-105">Os provedores usam tarefas e opcodes para agrupar eventos logicamente.</span><span class="sxs-lookup"><span data-stu-id="be4e7-105">Providers use tasks and opcodes to logically group events.</span></span> <span data-ttu-id="be4e7-106">O agrupamento de eventos ajuda os consumidores a consultar apenas os eventos que contêm combinações específicas de tarefa e opcode.</span><span class="sxs-lookup"><span data-stu-id="be4e7-106">Grouping events helps consumers query for only those events that contain specific task and opcode combinations.</span></span> <span data-ttu-id="be4e7-107">Normalmente, você usa tarefas para identificar um componente principal do provedor, como o componente de rede ou de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="be4e7-107">Typically, you use tasks to identify a major component of the provider such as the networking or database component.</span></span> <span data-ttu-id="be4e7-108">Em seguida, você pode usar opcodes para identificar as operações que o componente executa, como as operações de envio e recebimento para um componente de rede.</span><span class="sxs-lookup"><span data-stu-id="be4e7-108">You could then use opcodes to identify the operations that the component performs, such as the send and receive operations for a networking component.</span></span> <span data-ttu-id="be4e7-109">Se você tivesse apenas um componente, poderia usar a tarefa para refletir uma grande operação no componente, como conectar ou desconectar e usar opcode para refletir uma atividade dentro da operação, como ler o registro.</span><span class="sxs-lookup"><span data-stu-id="be4e7-109">If you had only one component, you could use task to reflect a major operation in the component, such as connect or disconnect, and use opcode to reflect an activity within the operation such as reading the registry.</span></span> <span data-ttu-id="be4e7-110">Você também pode usar o opcode sem especificar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="be4e7-110">You could also use opcode without specifying a task.</span></span> <span data-ttu-id="be4e7-111">A maneira como você usa a tarefa e os opcodes para agrupar eventos para o consumidor é completamente seu.</span><span class="sxs-lookup"><span data-stu-id="be4e7-111">How you use task and opcodes to group events for the consumer is completely up to you.</span></span>

<span data-ttu-id="be4e7-112">Para definir uma tarefa, use o elemento **Task** .</span><span class="sxs-lookup"><span data-stu-id="be4e7-112">To define a task, use the **task** element.</span></span> <span data-ttu-id="be4e7-113">Para definir um opcode, use o elemento **opcode** .</span><span class="sxs-lookup"><span data-stu-id="be4e7-113">To define an opcode, use the **opcode** element.</span></span> <span data-ttu-id="be4e7-114">Você pode especificar até 228 OpCodes.</span><span class="sxs-lookup"><span data-stu-id="be4e7-114">You can specify up to 228 opcodes.</span></span> <span data-ttu-id="be4e7-115">O **valor** da tarefa deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="be4e7-115">The task **value** must be greater than 0.</span></span> <span data-ttu-id="be4e7-116">Os opcodes devem estar no intervalo de 11 a 239.</span><span class="sxs-lookup"><span data-stu-id="be4e7-116">The opcodes must be in the range from 11 through 239.</span></span> <span data-ttu-id="be4e7-117">O arquivo de Winmeta.xml define operações comuns que você pode usar em vez de definir as suas próprias.</span><span class="sxs-lookup"><span data-stu-id="be4e7-117">The Winmeta.xml file defines common operations that you can use instead of defining your own.</span></span>

<span data-ttu-id="be4e7-118">O exemplo a seguir mostra como definir várias tarefas e OpCodes.</span><span class="sxs-lookup"><span data-stu-id="be4e7-118">The following example shows how to define several tasks and opcodes.</span></span>

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
