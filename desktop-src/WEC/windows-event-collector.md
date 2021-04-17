---
title: Coletor de Eventos do Windows
description: Você pode assinar para receber e armazenar eventos em um computador local (coletor de eventos) que são encaminhados de um computador remoto (origem do evento).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813212"
---
# <a name="windows-event-collector"></a>Coletor de Eventos do Windows

Você pode assinar para receber e armazenar eventos em um computador local (coletor de eventos) que são encaminhados de um computador remoto (origem do evento). As [funções do coletor de eventos do Windows](windows-event-collector-functions.md) dão suporte à assinatura de eventos usando o protocolo WS-Management. Para obter mais informações sobre o WS-Management, consulte [about gerenciamento remoto do Windows](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Arquitetura de coleta de eventos e encaminhamento de eventos

A coleta de eventos permite que os administradores obtenham eventos de computadores remotos e os armazenem em um log de eventos local no computador do coletor. O caminho do log de destino para os eventos é uma propriedade da assinatura. Todos os dados no evento encaminhado são salvos no log de eventos do computador do coletor (nenhuma das informações é perdida). Informações adicionais relacionadas ao encaminhamento de eventos também são adicionadas ao evento. Para obter mais informações sobre como habilitar um computador para receber eventos coletados ou encaminhar eventos, consulte [configurar computadores para encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Assinaturas

A lista a seguir descreve os tipos de assinaturas de evento:

-   Assinaturas iniciadas pela origem: permite que você defina uma assinatura de evento em um computador do coletor de eventos sem definir os computadores de origem do evento. Vários computadores de origem de evento remoto podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos. Para obter mais informações, consulte [Configurando uma assinatura iniciada pela fonte](setting-up-a-source-initiated-subscription.md). Esse tipo de assinatura é útil quando você não sabe ou não deseja especificar todos os computadores de origens de eventos que encaminharão eventos.
-   Assinaturas iniciadas pelo coletor: permite que você crie uma assinatura de evento se você souber todos os computadores de origem do evento que encaminharão eventos. Você especifica todas as origens de evento no momento em que a assinatura é criada. Para obter mais informações, consulte [criando uma assinatura iniciada pelo coletor](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Funções do coletor de eventos do Windows

Para obter mais informações e exemplos de código que usam as funções do coletor de eventos, consulte [usando o coletor de eventos do Windows](using-windows-event-collector.md).

Para obter mais informações sobre as funções usadas para coletar e encaminhar eventos, consulte [funções do coletor de eventos do Windows](windows-event-collector-functions.md).

 

 