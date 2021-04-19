---
description: Cada log na chave EventLog contém subchaves chamadas fontes de eventos. A origem do evento é o nome do software que registra o evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Origens de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780548"
---
# <a name="event-sources"></a><span data-ttu-id="a9614-104">Origens de eventos</span><span class="sxs-lookup"><span data-stu-id="a9614-104">Event Sources</span></span>

<span data-ttu-id="a9614-105">Cada log na [chave EventLog](eventlog-key.md) contém subchaves chamadas *fontes de eventos*.</span><span class="sxs-lookup"><span data-stu-id="a9614-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="a9614-106">A origem do evento é o nome do software que registra o evento.</span><span class="sxs-lookup"><span data-stu-id="a9614-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="a9614-107">Geralmente, é o nome do aplicativo ou o nome de um subcomponente do aplicativo se o aplicativo for grande.</span><span class="sxs-lookup"><span data-stu-id="a9614-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="a9614-108">Você pode adicionar um máximo de 16.384 origens de eventos ao registro.</span><span class="sxs-lookup"><span data-stu-id="a9614-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="a9614-109">O log de **segurança** é somente para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9614-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="a9614-110">Os drivers de dispositivo devem adicionar seus nomes ao log do **sistema** .</span><span class="sxs-lookup"><span data-stu-id="a9614-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="a9614-111">Os aplicativos e serviços devem adicionar seus nomes ao log do **aplicativo** ou criar um log personalizado.</span><span class="sxs-lookup"><span data-stu-id="a9614-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="a9614-112">A estrutura das origens do evento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9614-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="a9614-113">Você não pode usar um nome de origem que já tenha sido usado como um nome de log.</span><span class="sxs-lookup"><span data-stu-id="a9614-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="a9614-114">Além disso, os nomes de origem não podem ser hierárquicos; ou seja, eles não podem conter o caractere de barra invertida (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="a9614-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="a9614-115">Cada origem de evento contém informações (como um [arquivo de mensagem](message-files.md)) específicas para o software que registrará os eventos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9614-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a9614-116">Valor do registro</span><span class="sxs-lookup"><span data-stu-id="a9614-116">Registry Value</span></span></th>
<th><span data-ttu-id="a9614-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9614-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9614-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="a9614-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="a9614-119">Número de categorias de eventos com suporte.</span><span class="sxs-lookup"><span data-stu-id="a9614-119">Number of event categories supported.</span></span> <span data-ttu-id="a9614-120">Esse valor é do tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9614-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9614-121"><strong>CategoryMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="a9614-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="a9614-122">Caminho para o arquivo de mensagem de categoria.</span><span class="sxs-lookup"><span data-stu-id="a9614-122">Path to the category message file.</span></span> <span data-ttu-id="a9614-123">Um arquivo de mensagem de categoria contém cadeias de caracteres dependentes de idioma que descrevem as categorias.</span><span class="sxs-lookup"><span data-stu-id="a9614-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="a9614-124">Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9614-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9614-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="a9614-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="a9614-126">Caminho para um ou mais arquivos de mensagem de evento; Use um ponto e vírgula para delimitar vários arquivos.</span><span class="sxs-lookup"><span data-stu-id="a9614-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="a9614-127">Um arquivo de mensagem de evento contém cadeias de caracteres dependentes de idioma que descrevem os eventos.</span><span class="sxs-lookup"><span data-stu-id="a9614-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="a9614-128">Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9614-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9614-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="a9614-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="a9614-130">Caminho para o arquivo de mensagem de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a9614-130">Path to the parameter message file.</span></span> <span data-ttu-id="a9614-131">Um arquivo de mensagem de parâmetro contém cadeias de caracteres independentes de idioma que devem ser inseridas nas cadeias de caracteres de descrição do evento.</span><span class="sxs-lookup"><span data-stu-id="a9614-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="a9614-132">Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9614-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9614-133"><strong>TypesSupported</strong></span><span class="sxs-lookup"><span data-stu-id="a9614-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="a9614-134">Bitmask de tipos com suporte.</span><span class="sxs-lookup"><span data-stu-id="a9614-134">Bitmask of supported types.</span></span> <span data-ttu-id="a9614-135">Esse valor é do tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9614-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="a9614-136">Pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a9614-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="a9614-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="a9614-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="a9614-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="a9614-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="a9614-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="a9614-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="a9614-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="a9614-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="a9614-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="a9614-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a9614-142">Quando um aplicativo usa a função [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para obter um identificador para um log de eventos, o serviço de log de eventos pesquisa a origem do evento especificado no registro.</span><span class="sxs-lookup"><span data-stu-id="a9614-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="a9614-143">Por exemplo, o log do **aplicativo** pode conter fontes de eventos para Microsoft SQL Server e o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a9614-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="a9614-144">Se um aplicativo usar [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou **OpenEventLog** com um nome de origem de aplicativo, SQL ou Excel, o serviço de log de eventos retornará um identificador para o log do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="a9614-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="a9614-145">Um aplicativo pode usar o log do **aplicativo** sem adicionar uma nova origem do evento ao registro.</span><span class="sxs-lookup"><span data-stu-id="a9614-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="a9614-146">Se o aplicativo chamar [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) e passar um nome de origem que não pode ser encontrado no registro, o serviço de log de eventos usará o log do **aplicativo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="a9614-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="a9614-147">No entanto, como não há nenhum arquivo de mensagem, o Visualizador de Eventos não pode mapear nenhum identificador de evento ou categorias de evento para uma cadeia de caracteres de descrição e exibirá um erro.</span><span class="sxs-lookup"><span data-stu-id="a9614-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="a9614-148">Por esse motivo, você deve adicionar uma origem de evento exclusiva ao registro para seu aplicativo e especificar um arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a9614-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



