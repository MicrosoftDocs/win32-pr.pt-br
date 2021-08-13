---
title: A interface IAccessibleEx
description: Controles que não têm um provedor microsoft Automação da Interface do Usuário, mas que implementam IAccessible, podem ser atualizados facilmente para fornecer algumas funcionalidades Automação da Interface do Usuário implementando a interface IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170e6160a05350fa459090b2f51dbedd618ebdb81512a7e9730b50f8533ef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566007"
---
# <a name="the-iaccessibleex-interface"></a>A interface IAccessibleEx

Controles que não têm um provedor microsoft Automação da Interface do Usuário, mas que implementam [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), podem ser atualizados facilmente para fornecer algumas funcionalidades Automação da Interface do Usuário implementando a interface [**IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Essa interface permite que o controle exponha Automação da Interface do Usuário propriedades e padrões de controle, sem a necessidade de uma implementação completa de interfaces de provedor Automação da Interface do Usuário como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para usar **IAccessibleEx,** **IRawElementProviderFragment** e todas as outras interfaces Automação da Interface do Usuário, inclua o arquivo de título UIAutomation.h no código-fonte.

Por exemplo, considere um controle personalizado que tenha um valor de intervalo. O Microsoft Active Accessibility para o controle define a função do controle e é capaz de retornar seu valor atual. No entanto, como Microsoft Active Accessibility define propriedades mínimas e máximas, o servidor não tem os meios para retornar os valores mínimo e máximo do controle. Um Automação da Interface do Usuário cliente é capaz de recuperar a função do controle, o valor atual e outras propriedades Microsoft Active Accessibility, pois o núcleo Automação da Interface do Usuário pode obter isso por meio de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). No entanto, sem acesso a uma interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) no objeto, o Automação da Interface do Usuário também não pode recuperar os valores máximo e mínimo.

O desenvolvedor de controle pode fornecer um provedor de Automação da Interface do Usuário completo para o controle, mas isso significa duplicar grande parte da funcionalidade existente da implementação [**de IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por exemplo, navegação e propriedades comuns. Em vez disso, o desenvolvedor pode continuar a depender de **IAccessible** para fornecer essa funcionalidade, adicionando suporte para propriedades específicas do controle por meio [**de IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>Nesta seção

-   [Diretrizes de implementação do IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementando IAccessibleEx para provedores](implementing-iaccessibleex-for-providers.md)
-   [Usando IAccessibleEx de um cliente](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Infraestrutura comum](common-infrastructure.md)
</dt> </dl>

 

 




