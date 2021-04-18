---
description: O WMI dá suporte a modelos de Threading diferentes, dependendo de como o provedor é hospedado e do tipo de funcionalidade do provedor, como classe ou propriedade.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Escolhendo o registro correto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771420"
---
# <a name="choosing-correct-registration"></a>Escolhendo o registro correto

O WMI dá suporte a modelos de Threading diferentes, dependendo de como o provedor é hospedado e do tipo de funcionalidade do provedor, como [classe](writing-a-class-provider.md) ou [Propriedade](writing-a-property-provider.md). Por exemplo, os [*provedores dissociados*](gloss-d.md) não oferecem suporte a todos os tipos de funcionalidade do provedor. Para obter mais informações sobre modelos de hospedagem diferentes e como configurá-los, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>Provedores de In-Process

Os provedores em processo são executados em um processo de host compartilhado, Wmiprvse.exe. A maioria dos tipos de provedor em processo usa o modelo de MTA (multithreaded apartment).

O modelo MTA tem suporte para os seguintes tipos de funcionalidade de provedor:

-   [Provedor de classe](writing-a-class-provider.md)
-   [Provedor de instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de propriedades](writing-a-property-provider.md)
-   [Provedor de eventos](writing-an-event-provider.md)
-   [Provedor de consumidor de eventos](writing-an-event-consumer-provider.md)

O modelo STA (single-threaded apartment) tem suporte para alguns tipos de funcionalidade de provedor:

-   [Provedor de instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de eventos](writing-an-event-provider.md)
-   [Provedor de consumidor de eventos](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Provedores fora do processo

Provedores que são hospedados em um host de serviço compartilhado diferente dão suporte à seguinte funcionalidade de provedor:

-   [Provedor de classe](writing-a-class-provider.md)
-   [Provedor de instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de propriedades](writing-a-property-provider.md)
-   [Provedor de eventos](writing-an-event-provider.md)
-   [Provedor de consumidor de eventos](writing-an-event-consumer-provider.md)

Para obter mais informações sobre hosts de serviço compartilhado, consulte [Hospedagem de provedor e segurança](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Provedores dissociados

Os provedores dissociados são hospedados em um aplicativo. Para obter mais informações, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md). Os provedores criados usando o WMI no .NET Framework são separados. Os provedores dissociados oferecem suporte à seguinte funcionalidade de provedor:

-   [Provedor de instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de eventos](writing-an-event-provider.md)
-   [Provedor de consumidor de eventos](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedagem e segurança de provedor](provider-hosting-and-security.md)
</dt> </dl>

 

 



