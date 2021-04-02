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
# <a name="securing-wmi-events"></a><span data-ttu-id="16031-104">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="16031-104">Securing WMI Events</span></span>

<span data-ttu-id="16031-105">Os eventos WMI são entregues pelo [*provedor de eventos*](gloss-e.md) a um consumidor [*temporário*](gloss-t.md) ou [*permanente*](gloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="16031-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="16031-106">O sistema de eventos WMI usa a comparação de [*descritores de segurança*](gloss-s.md) em eventos e [*SIDs*](gloss-s.md) de conta de usuário para controlar o acesso ao evento.</span><span class="sxs-lookup"><span data-stu-id="16031-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="16031-107">Os eventos são entregues na forma de uma instância de uma classe de evento normalmente, mas não necessariamente, derivados definitivamente do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="16031-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="16031-108">O WMI fornece várias classes de evento gerais nas [classes do sistema WMI](wmi-system-classes.md), como [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="16031-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="16031-109">Os provedores também podem fornecer suas próprias classes de evento.</span><span class="sxs-lookup"><span data-stu-id="16031-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="16031-110">Por exemplo, o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) tem classes de evento que relatam a alteração de uma chave ou um valor do registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="16031-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="16031-111">Os tópicos a seguir fornecem informações sobre como proteger a entrega de eventos para provedores e receber eventos com segurança para scripts e aplicativos de cliente:</span><span class="sxs-lookup"><span data-stu-id="16031-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="16031-112">Fornecendo eventos com segurança</span><span class="sxs-lookup"><span data-stu-id="16031-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="16031-113">Recebendo eventos com segurança</span><span class="sxs-lookup"><span data-stu-id="16031-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="16031-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16031-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16031-115">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="16031-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
