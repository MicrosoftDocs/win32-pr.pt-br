---
description: Quando o usuário inicia Visualizador de Eventos para exibir as entradas do log de eventos, ele chama a função ReadEventLog para obter as estruturas EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Exibindo o log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165446"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="9ef1b-103">Exibindo o log de eventos</span><span class="sxs-lookup"><span data-stu-id="9ef1b-103">Viewing the Event Log</span></span>

<span data-ttu-id="9ef1b-104">Quando o usuário inicia Visualizador de Eventos para exibir as entradas do log de eventos, ele chama a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para obter as estruturas [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="9ef1b-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="9ef1b-105">O Visualizador de Eventos usa a origem do evento e o identificador de evento para obter o texto da mensagem para cada evento do arquivo de mensagem registrado (indicado pelo valor do registro **EventMessageFile** para a origem).</span><span class="sxs-lookup"><span data-stu-id="9ef1b-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="9ef1b-106">O Visualizador de Eventos usa a função [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para carregar o arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ef1b-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="9ef1b-107">Em seguida, o Visualizador de Eventos usa a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para recuperar a cadeia de caracteres de descrição base do módulo carregado.</span><span class="sxs-lookup"><span data-stu-id="9ef1b-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="9ef1b-108">Por fim, o Visualizador de Eventos substitui os parâmetros de inserção na cadeia de caracteres de descrição base para gerar a cadeia de caracteres final da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ef1b-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
