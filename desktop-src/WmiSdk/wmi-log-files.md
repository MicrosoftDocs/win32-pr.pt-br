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
# <a name="wmi-log-files"></a>Arquivos de log do WMI

O WMI usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e os eventos podem ser obtidos por meio da interface do usuário **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

-   [Rastreamento de eventos em vez de logs de texto](#event-tracing-instead-of-text-logs)
-   [Arquivos de log do WMI](#wmi-log-files)
-   [Tópicos relacionados](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Rastreamento de eventos em vez de logs de texto

A atividade do serviço WMI é registrada no arquivo WMITracing. log. Para obter mais informações sobre como habilitar o rastreamento de eventos WMI e acessar o arquivo WMITracing. log, consulte [rastreando a atividade WMI](tracing-wmi-activity.md). Os provedores de Windows Driver Model (WDM) continuam a fazer logon no arquivo Wbemprov. log.

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

 

 
