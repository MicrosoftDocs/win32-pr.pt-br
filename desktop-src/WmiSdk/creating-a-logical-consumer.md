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
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="2cc34-103">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="2cc34-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="2cc34-104">Um consumidor lógico é uma instância de uma classe de consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="2cc34-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="2cc34-105">A principal finalidade de um consumidor lógico é fornecer ao consumidor físico os parâmetros para as atividades que o consumidor físico realiza.</span><span class="sxs-lookup"><span data-stu-id="2cc34-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="2cc34-106">Para obter mais informações, consulte [criando uma nova classe de consumidor de evento permanente](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="2cc34-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="2cc34-107">O consumidor permanente deve ter o mesmo [**CreatorSID**](--eventconsumer.md) nas instâncias de consumidor, filtro e associação.</span><span class="sxs-lookup"><span data-stu-id="2cc34-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="2cc34-108">Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="2cc34-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="2cc34-109">Para obter um exemplo de como usar um consumidor lógico, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md), que mostra o uso da classe de consumidor padrão [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para configurar um consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="2cc34-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="2cc34-110">O procedimento a seguir descreve como criar um consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="2cc34-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="2cc34-111">**Para criar um consumidor lógico**</span><span class="sxs-lookup"><span data-stu-id="2cc34-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="2cc34-112">Crie uma instância de sua classe de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="2cc34-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="2cc34-113">Preencha as propriedades da instância com os parâmetros da ação que você deseja que o consumidor físico execute.</span><span class="sxs-lookup"><span data-stu-id="2cc34-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="2cc34-114">O exemplo de código MOF a seguir descreve um consumidor lógico que contém um script.</span><span class="sxs-lookup"><span data-stu-id="2cc34-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

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

<span data-ttu-id="2cc34-115">Depois de criar o consumidor lógico, você deve vincular cada filtro a um filtro de eventos para atribuir a ação a um evento específico.</span><span class="sxs-lookup"><span data-stu-id="2cc34-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="2cc34-116">Para obter mais informações, consulte [criando um filtro de eventos](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2cc34-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



