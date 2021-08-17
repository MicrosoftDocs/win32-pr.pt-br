---
description: O WMI usa o ETW (rastreamento de eventos) e os eventos podem ser obtidos por meio da interface do usuário Visualizador de Eventos ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte Rastreando a atividade WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Arquivos de log do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fff9064dd82484568282f649b3380f544d9ba58a569e36583664806d47b5e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739423"
---
# <a name="wmi-log-files"></a>Arquivos de log do WMI

O WMI usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e os eventos podem ser obtidos por meio da interface do usuário **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

-   [Rastreamento de eventos em vez de logs de texto](#event-tracing-instead-of-text-logs)
-   [Arquivos de log do WMI](#wmi-log-files)
-   [Tópicos relacionados](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Rastreamento de eventos em vez de logs de texto

A atividade do serviço WMI é registrada no arquivo WMITracing. log. Para obter mais informações sobre como habilitar o rastreamento de eventos WMI e acessar o arquivo WMITracing. log, consulte [rastreando a atividade WMI](tracing-wmi-activity.md). Windows Provedores de modelo de driver (WDM) continuam a fazer logon no arquivo Wbemprov. log.

## <a name="wmi-log-files"></a>Arquivos de log do WMI

O serviço WMI e alguns provedores gravam arquivos de log de texto para registrar eventos.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Arquivos de log do provedor WMI](wmi-provider-log-files.md)
</dt> <dd>

Os provedores de WMI também podem manter logs. Quais arquivos de log aparecem em um sistema depende de quais provedores estão instalados.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> <dt>

[Rastreando a atividade WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrando em log a atividade WMI](logging-wmi-activity.md)
</dt> </dl>

 

 
