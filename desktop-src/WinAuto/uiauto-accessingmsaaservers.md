---
title: Acessando servidores Microsoft Acessibilidade Ativa
description: O Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário é um componente de software que permite que os clientes da automação da interface do usuário da Microsoft interajam com os servidores do Microsoft Acessibilidade Ativa que implementam a interface IAccessible nativamente.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automação da interface do usuário, acessando Acessibilidade Ativa
- Automação da interface do usuário, Acessibilidade Ativa
- Proxy de automação da interface do usuário
- Automação da interface do usuário, proxy de automação da IU
- Padrão de controle LegacyIAccessible
- Automação da interface do usuário, padrão de controle LegacyIAccessible
- Acessibilidade Ativa da Microsoft
- Acessibilidade Ativa
- clientes, acessando servidores Acessibilidade Ativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6f6ccbc29695b7ca5d1413025a50a7bcf4a9cf679dbcd6a0b8f3160ff0b399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030766"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Acessando servidores Microsoft Acessibilidade Ativa

O Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário é um componente de software que permite que os clientes da automação da interface do usuário da Microsoft interajam com os servidores do Microsoft Acessibilidade Ativa que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativamente. O proxy dá suporte ao padrão de controle [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) e fornece uma instância da interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para cada servidor do Microsoft acessibilidade ativa detectado. Os clientes de automação da interface do usuário usam os métodos expostos por **IUIAutomationLegacyIAccessiblePattern** para acessar as propriedades do Microsoft acessibilidade ativa e os objetos com suporte no servidor.

Se um elemento de automação da interface do usuário tiver uma implementação subjacente do Microsoft Acessibilidade Ativa, um cliente poderá obter um ponteiro de interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para o elemento, passando a ID do padrão de controle [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) para um dos seguintes métodos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

A interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) não está disponível para controles baseados na automação da interface do usuário.

A interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permite que clientes de automação da interface do usuário acessem a implementação base do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um elemento Microsoft acessibilidade ativa. No entanto, a interface não oferece suporte a métodos obsoletos ou redundantes com recursos de automação da interface do usuário. Por exemplo, **IUIAutomationLegacyIAccessiblePattern** não tem um método equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque o local atual de um elemento de interface do usuário está disponível na propriedade BoundingRectangle de automação da interface do usuário.

O método [**IUIAutomationLegacyIAccessiblePattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permite que um cliente recupere um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um elemento de automação de interface do usuário. O inverso também é possível usando os métodos [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .

[**IUIAutomationLegacyIAccessiblePattern:: getiaccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) retornará **nulo** se a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do elemento for fornecida por um objeto proxy de OLEACC.dll ou da automação da interface do usuário para o Microsoft acessibilidade ativa Bridge.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Automação e Acessibilidade Ativa da interface do usuário](uiauto-msaa.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




