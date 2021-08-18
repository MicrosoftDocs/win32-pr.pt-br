---
title: Coletor de Eventos do Windows
description: Você pode assinar para receber e armazenar eventos em um computador local (coletor de eventos) que são encaminhados de um computador remoto (origem do evento).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efa767ecb80960fc3461380435ea1d44992656d7c67df990574f7155ee976fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997876"
---
# <a name="windows-event-collector"></a>Coletor de Eventos do Windows

Você pode assinar para receber e armazenar eventos em um computador local (coletor de eventos) que são encaminhados de um computador remoto (origem do evento). As [Windows funções do Coletor de](windows-event-collector-functions.md) Eventos do WS-Management suportam a assinatura de eventos usando o protocolo WS-Management dados. Para obter mais informações sobre o WS-Management, consulte [About Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Arquitetura de coleta de eventos e encaminhamento de eventos

A coleta de eventos permite que os administradores recebam eventos de computadores remotos e armazenem-os em um log de eventos local no computador coletor. O caminho de log de destino para os eventos é uma propriedade da assinatura. Todos os dados no evento encaminhado são salvos no log de eventos do computador coletor (nenhuma das informações é perdida). Informações adicionais relacionadas ao encaminhamento de eventos também são adicionadas ao evento. Para obter mais informações sobre como habilitar um computador a receber eventos coletados ou encaminhar eventos, consulte Configurar computadores para [encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Assinaturas

A lista a seguir descreve os tipos de assinaturas de evento:

-   Assinaturas iniciadas por origem: permite que você defina uma assinatura de evento em um computador coletor de eventos sem definir os computadores de origem do evento. Vários computadores de origem de eventos remotos podem ser então definidos (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos. Para obter mais informações, consulte [Configurando uma assinatura iniciada por origem.](setting-up-a-source-initiated-subscription.md) Esse tipo de assinatura é útil quando você não sabe ou não deseja especificar todos os computadores de origem do evento que encaminharão eventos.
-   Assinaturas iniciadas pelo coletor: permite que você crie uma assinatura de evento se você conhecer todos os computadores de origem do evento que encaminharão eventos. Você especifica todas as fontes de evento no momento em que a assinatura é criada. Para obter mais informações, consulte [Criando uma assinatura iniciada pelo coletor](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Windows Funções do Coletor de Eventos

Para obter mais informações e exemplos de código que usam as funções do Coletor de Eventos, consulte [Using Windows Event Collector](using-windows-event-collector.md).

Para obter mais informações sobre as funções usadas para coletar e encaminhar eventos, [consulte funções Windows Coletor de Eventos](windows-event-collector-functions.md).

 

 