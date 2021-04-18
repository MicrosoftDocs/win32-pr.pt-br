---
description: O WMI usa o ETW (rastreamento de eventos) e os eventos podem ser obtidos por meio da interface do usuário Visualizador de Eventos ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte Rastreando a atividade WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Arquivos de log do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781239"
---
# <a name="wmi-log-files"></a><span data-ttu-id="767f2-104">Arquivos de log do WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-104">WMI Log Files</span></span>

<span data-ttu-id="767f2-105">O WMI usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e os eventos podem ser obtidos por meio da interface do usuário **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="767f2-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="767f2-106">Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="767f2-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="767f2-107">Rastreamento de eventos em vez de logs de texto</span><span class="sxs-lookup"><span data-stu-id="767f2-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="767f2-108">Arquivos de log do WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="767f2-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="767f2-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="767f2-110">Rastreamento de eventos em vez de logs de texto</span><span class="sxs-lookup"><span data-stu-id="767f2-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="767f2-111">A atividade do serviço WMI é registrada no arquivo WMITracing. log.</span><span class="sxs-lookup"><span data-stu-id="767f2-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="767f2-112">Para obter mais informações sobre como habilitar o rastreamento de eventos WMI e acessar o arquivo WMITracing. log, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="767f2-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="767f2-113">Os provedores de Windows Driver Model (WDM) continuam a fazer logon no arquivo Wbemprov. log.</span><span class="sxs-lookup"><span data-stu-id="767f2-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="767f2-114">Arquivos de log do WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-114">WMI Log Files</span></span>

<span data-ttu-id="767f2-115">O serviço WMI e alguns provedores gravam arquivos de log de texto para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="767f2-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="767f2-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Arquivos de log do provedor WMI](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="767f2-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="767f2-117">Os provedores de WMI também podem manter logs.</span><span class="sxs-lookup"><span data-stu-id="767f2-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="767f2-118">Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.</span><span class="sxs-lookup"><span data-stu-id="767f2-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="767f2-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="767f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="767f2-120">Referência de WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="767f2-121">Rastreando a atividade WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="767f2-122">Registrando em log a atividade WMI</span><span class="sxs-lookup"><span data-stu-id="767f2-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
