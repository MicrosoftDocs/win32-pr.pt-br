---
description: O WMI dá suporte a modelos de threading diferentes, dependendo de como o provedor está hospedado e do tipo de funcionalidade do provedor, como Classe ou Propriedade.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Escolhendo o registro correto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a252e9013e828f5dc2c6e4c7228919d0834d0edb3da5f699cbe0306a38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131798"
---
# <a name="choosing-correct-registration"></a>Escolhendo o registro correto

O WMI dá suporte a diferentes modelos de threading, dependendo de como o provedor está hospedado e do tipo de funcionalidade do provedor, como [Classe](writing-a-class-provider.md) ou [Propriedade](writing-a-property-provider.md). Por exemplo, [*provedores desaparados*](gloss-d.md) não suportam todos os tipos de funcionalidade do provedor. Para obter mais informações sobre diferentes modelos de hospedagem e como configurá-los, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)

## <a name="in-process-providers"></a>provedores In-Process dados

Os provedores em processo são executados em um processo de host compartilhado, Wmiprvse.exe. A maioria dos tipos de provedor em processo usa o modelo MTA (multithreaded apartment).

O modelo MTA tem suporte para os seguintes tipos de funcionalidade do provedor:

-   [Provedor de Classe](writing-a-class-provider.md)
-   [Provedor de Instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de propriedades](writing-a-property-provider.md)
-   [Provedor de Eventos](writing-an-event-provider.md)
-   [Provedor de Consumidor de Eventos](writing-an-event-consumer-provider.md)

O modelo STA (single-threaded apartment) tem suporte para alguns tipos de funcionalidade do provedor:

-   [Provedor de Instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de Eventos](writing-an-event-provider.md)
-   [Provedor de Consumidor de Eventos](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Provedores fora do processo

Provedores hospedados em um host de serviço compartilhado diferente suportam a seguinte funcionalidade de provedor:

-   [Provedor de Classe](writing-a-class-provider.md)
-   [Provedor de Instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de propriedades](writing-a-property-provider.md)
-   [Provedor de Eventos](writing-an-event-provider.md)
-   [Provedor de Consumidor de Eventos](writing-an-event-consumer-provider.md)

Para obter mais informações sobre hosts de serviço compartilhado, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)

## <a name="decoupled-providers"></a>Provedores desaplados

Provedores desaplados são hospedados em um aplicativo. Para obter mais informações, [consulte Incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md). Os provedores criados usando o WMI no .NET Framework são desacoplados. Os provedores desaparados suportam a seguinte funcionalidade de provedor:

-   [Provedor de Instância](writing-an-instance-provider.md)
-   [Provedor de método](writing-a-method-provider.md)
-   [Provedor de Eventos](writing-an-event-provider.md)
-   [Provedor de Consumidor de Eventos](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedagem e segurança do provedor](provider-hosting-and-security.md)
</dt> </dl>

 

 



