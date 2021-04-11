---
description: Você pode impedir que usuários não autorizados recebam eventos aos quais eles não devem ter acesso.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Fornecendo eventos com segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170888"
---
# <a name="providing-events-securely"></a>Fornecendo eventos com segurança

Você pode impedir que usuários não autorizados recebam eventos aos quais eles não devem ter acesso. Seu provedor de eventos pode fornecer instâncias de suas próprias classes de evento, assim como o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) fornece classes como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Seu provedor de eventos também pode fornecer eventos intrínsecos, como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md). Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).

Um provedor de eventos pode controlar o acesso a destinatários de eventos das seguintes maneiras:

-   Usando o controle de acesso implementando [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) é a maneira mais eficiente.

    O provedor determina se o consumidor tem privilégios para receber um evento solicitado. Se o consumidor não tem privilégios suficientes para se registrar, o WMI retorna um erro de acesso negado. Use esse modo quando o provedor puder tomar a decisão sobre quem pode receber eventos. Por exemplo, um provedor pode fornecer eventos relacionados à segurança e pode exigir que o consumidor tenha privilégios de administrador com o privilégio **SeSecurityPrivilege** habilitado.

-   Implementar [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) no coletor usado para gerar eventos permite a configuração de um descritor de segurança (SD) em um coletor para todos os eventos transmitidos.

    O WMI executa verificações de acesso com base no SD. Use esse modo quando o provedor não puder tomar a decisão em relação a quem tem permissão para consumir seus eventos, mas pode decidir em um SD para um coletor específico. Por exemplo, use [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) se seu provedor de eventos obtiver vários coletores por chamadas para [**IWbemEventSink:: GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) e você quiser um descritor de segurança para cada coletor.

-   A definição da propriedade **\_ descritor de segurança** de um evento permite a configuração de um SD para cada evento.

    Use essa abordagem quando cada evento entregue ao coletor puder ter descritores de segurança diferentes. Para usar essa abordagem, derive qualquer uma das classes de evento extrínsecos definidas pelo seu provedor de [**\_ \_ Event**](--event.md) ou [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) para que sua classe contenha a propriedade do **\_ descritor de segurança** . Por exemplo, seu provedor de eventos pode publicar eventos seguros e normais por meio de um coletor. Nesse caso, use o descritor de segurança da conta administradores para eventos seguros e um descritor de segurança **nulo** para eventos normais que podem ser recebidos por qualquer pessoa.

## <a name="securing-events-by-decoupled-event-providers"></a>Protegendo eventos por provedores de eventos dissociados

Os provedores de eventos dissociados diferem dos provedores de eventos nondecoupled da maneira como se registram com o WMI. A chamada para [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) para eventos de um provedor desacoplado nunca propaga o token de acesso do cliente. O WMI manipula o controle de acesso da mesma maneira que para provedores de eventos nondecoupled. Para obter mais informações sobre como gravar um provedor dissociado, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).

Somente os administradores com o privilégio de **\_ gravação total** definido no **controle WMI** do **painel de controle** têm permissão para gerar eventos para um namespace. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 
