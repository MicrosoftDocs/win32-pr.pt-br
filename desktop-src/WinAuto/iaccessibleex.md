---
title: A interface IAccessibleEx
description: Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o IAccessible, podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário implementando a interface IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084107"
---
# <a name="the-iaccessibleex-interface"></a>A interface IAccessibleEx

Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Essa interface permite que o controle exponha Propriedades de automação da interface do usuário e padrões de controle, sem a necessidade de uma implementação completa das interfaces do provedor de automação da interface do usuário, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para usar **IAccessibleEx**, **IRawElementProviderFragment** e todas as outras interfaces de automação de interface do usuário, inclua o arquivo de cabeçalho automação da IU. h em seu código-fonte.

Por exemplo, considere um controle personalizado que tem um valor de intervalo. O Microsoft Acessibilidade Ativa Server para o controle define a função do controle e é capaz de retornar seu valor atual. No entanto, como o Microsoft Acessibilidade Ativa não define as propriedades mínima e máxima, o servidor não tem os meios para retornar os valores mínimo e máximo do controle. Um cliente de automação de interface do usuário é capaz de recuperar a função do controle, o valor atual e outras propriedades do Microsoft Acessibilidade Ativa, porque o núcleo de automação da interface do usuário pode obtê-los por meio do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). No entanto, sem acesso a uma interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) no objeto, a automação da interface do usuário também não consegue recuperar os valores mínimo e máximo.

O desenvolvedor de controle poderia fornecer um provedor de automação de interface do usuário completo para o controle, mas isso significaria duplicar grande parte da funcionalidade existente da implementação do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por exemplo, navegação e propriedades comuns. Em vez disso, o desenvolvedor pode continuar a confiar no **IAccessible** para fornecer essa funcionalidade, ao mesmo tempo em que adiciona suporte para propriedades específicas de controle por meio de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>Nesta seção

-   [Diretrizes de implementação do IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementando IAccessibleEx para provedores](implementing-iaccessibleex-for-providers.md)
-   [Usando o IAccessibleEx de um cliente](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Infraestrutura comum](common-infrastructure.md)
</dt> </dl>

 

 




