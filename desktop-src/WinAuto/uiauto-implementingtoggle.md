---
title: Alternar padrão de controle
description: Descreve as diretrizes e convenções para implementar o IToggleProvider, incluindo informações sobre propriedades e métodos. O padrão de controle toggle é usado para dar suporte a controles que podem percorrer um conjunto de Estados e manter um estado depois de definido.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automação da interface do usuário, implementando o padrão de controle toggle
- Automação da interface do usuário, alternar padrão de controle
- Automação da interface do usuário, IToggleProvider
- IToggleProvider
- Implementando padrões de controle de alternância de automação de IU
- Alternar padrões de controle
- padrões de controle, IToggleProvider
- padrões de controle, implementando alternância de automação da interface do usuário
- padrões de controle, alternância
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363813"
---
# <a name="toggle-control-pattern"></a>Alternar padrão de controle

Descreve as diretrizes e convenções para implementar o [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **Toggle** é usado para dar suporte a controles que podem percorrer um conjunto de Estados e manter um estado depois de definido.

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IToggleProvider**](#required-members-for-itoggleprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **alternância** , observe as seguintes diretrizes e convenções:

-   Os controles que não mantêm o estado quando ativados, como botões, botões da barra de ferramentas e hiperlinks, devem implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) em vez disso.
-   Um controle deve percorrer seus Estados de alternância ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) na seguinte ordem: **ToggleState \_ ativado**, **ToggleState \_ desativado** e, se houver suporte, **ToggleState \_ indeterminado**.
-   A **alternância** não fornece um método set-state devido a problemas em torno da configuração direta de uma caixa de seleção de três Estados, sem passar pela sequência apropriada de [**alternância**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) .
-   O controle de botão de opção não implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), pois não é capaz de percorrer seus Estados válidos.

## <a name="required-members-for-itoggleprovider"></a>Membros necessários para **IToggleProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .



| Membros necessários                                          | Tipo de membro | Observações |
|-----------------------------------------------------------|-------------|-------|
| [**Alternar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Método      | Nenhum  |
| [**Alternânciastate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Propriedade    | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




