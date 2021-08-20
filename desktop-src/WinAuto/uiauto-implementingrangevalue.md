---
title: Padrão de controle RangeValue
description: Descreve as diretrizes e convenções para implementar o IRangeValueProvider, incluindo informações sobre propriedades e métodos. O padrão de controle RangeValue é usado para dar suporte a controles que podem ser definidos como um valor dentro de um intervalo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automação da interface do usuário, implementando o padrão de controle RangeValue
- Automação da interface do usuário, padrão de controle RangeValue
- Automação da interface do usuário, IRangeValueProvider
- IRangeValueProvider
- Implementando padrões de controle RangeValue de automação da interface do usuário
- Padrões de controle RangeValue
- padrões de controle, IRangeValueProvider
- padrões de controle, implementando intervalo de automação de interface do usuário
- padrões de controle, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114857"
---
# <a name="rangevalue-control-pattern"></a>Padrão de controle RangeValue

Descreve as diretrizes e convenções para implementar o [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **RangeValue** é usado para dar suporte a controles que podem ser definidos como um valor dentro de um intervalo.

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **RangeValue** , observe as seguintes diretrizes e convenções:

-   Os controles permitem a recalibração de suas propriedades com suporte com base na localidade ou na preferência do usuário. Um exemplo disso é um controle de termômetro que pode ser definido para exibir a temperatura em Fahrenheit ou Celsius.
-   Controles que têm valores de intervalo ambíguos, como barras de progresso ou controles deslizantes, devem ter esses valores normalizados.

## <a name="required-members-for-irangevalueprovider"></a>Membros necessários para **IRangeValueProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .



| Membros necessários                                              | Tipo de membro | Observações |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Propriedade    | Nenhum  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Propriedade    | Nenhum  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Propriedade    | Nenhum  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Propriedade    | Nenhum  |
| [**Máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Propriedade    | Nenhum  |
| [**Mínimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Propriedade    | Nenhum  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




