---
description: Os eventos WMI são entregues pelo provedor de eventos a um consumidor temporário ou permanente. O sistema de eventos WMI usa a comparação de descritores de segurança em eventos e SIDs de conta de usuário para controlar o acesso ao evento.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Protegendo eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165204"
---
# <a name="securing-wmi-events"></a>Protegendo eventos WMI

Os eventos WMI são entregues pelo [*provedor de eventos*](gloss-e.md) a um consumidor [*temporário*](gloss-t.md) ou [*permanente*](gloss-p.md) . O sistema de eventos WMI usa a comparação de [*descritores de segurança*](gloss-s.md) em eventos e [*SIDs*](gloss-s.md) de conta de usuário para controlar o acesso ao evento.

Os eventos são entregues na forma de uma instância de uma classe de evento normalmente, mas não necessariamente, derivados definitivamente do [**\_ \_ evento**](--event.md). O WMI fornece várias classes de evento gerais nas [classes do sistema WMI](wmi-system-classes.md), como [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md). Os provedores também podem fornecer suas próprias classes de evento. Por exemplo, o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) tem classes de evento que relatam a alteração de uma chave ou um valor do registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Os tópicos a seguir fornecem informações sobre como proteger a entrega de eventos para provedores e receber eventos com segurança para scripts e aplicativos de cliente:

-   [Fornecendo eventos com segurança](providing-events-securely.md)
-   [Recebendo eventos com segurança](receiving-events-securely.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
