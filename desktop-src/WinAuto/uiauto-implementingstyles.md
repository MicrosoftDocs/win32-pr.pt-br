---
title: Padrão de controle de estilos
description: Descreve as diretrizes e convenções para implementar o IStylesProvider, incluindo informações sobre propriedades e métodos. O padrão de controle de estilos é usado para descrever um elemento de interface do usuário que tem um estilo específico, cor de preenchimento, padrão de preenchimento ou forma.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automação da interface do usuário, implementação de padrões de controle de estilos
- Automação da interface do usuário, padrão de controle de estilos
- Automação da interface do usuário, IStylesProvider
- IStylesProvider
- Implementando o padrão de controle estilos de automação de interface
- Padrão de controle de estilos
- padrões de controle, IStylesProvider
- padrões de controle, implementação de estilos de automação da interface do usuário
- padrões de controle, estilos
- interfaces, IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641675"
---
# <a name="styles-control-pattern"></a>Padrão de controle de estilos

Descreve as diretrizes e convenções para implementar o [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), incluindo informações sobre propriedades e métodos. O padrão de controle de **estilos** é usado para descrever um elemento de interface do usuário que tem um estilo específico, cor de preenchimento, padrão de preenchimento ou forma.

O padrão de controle de **estilos** é especialmente útil para descrever elementos em um documento, que frequentemente têm esses estilos. Normalmente, os estilos carregam informações úteis para clientes com deficiências; por exemplo, um estilo pode descrever uma determinada cadeia de caracteres como o título de um documento ou um determinado objeto de fluxograma como um losango ou um círculo. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IStylesProvider**](#required-members-for-istylesprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **estilos** , observe as seguintes diretrizes e convenções:

-   O arquivo de cabeçalho UIAutomationClient. h define um conjunto de valores constantes nomeados usados para identificar vários estilos comuns. Para obter mais informações, consulte [**identificadores de estilo**](uiauto-style-identifiers.md).
-   Se você usar [**StyleID \_ personalizado**](uiauto-style-identifiers.md), deverá implementar a propriedade [**IStylesProvider:: styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que os clientes descubram o nome do estilo. Você não precisa implementar a propriedade **styleName** para um estilo padrão porque a automação da interface do usuário da Microsoft fornece um nome padrão, mas você pode implementá-la se precisar substituir o nome padrão.
-   As outras propriedades no padrão de **estilos** são opcionais; o provedor pode retornar [**UIA \_ E \_ sem suporte**](uiauto-error-codes.md) para uma propriedade que não tem suporte.
-   Os estilos em um intervalo de texto podem ser representados por meio dos seguintes atributos de texto:
    -   Ao responder a uma solicitação para o atributo de texto [**StyleID**](uiauto-textattribute-ids.md) , o intervalo de texto deve retornar um dos identificadores de estilo descritos em [**identificadores de estilo**](uiauto-style-identifiers.md).
    -   Se [**StyleID \_ personalizado**](uiauto-style-identifiers.md) for usado, o intervalo de texto deverá retornar um valor de cadeia de caracteres para o atributo de texto [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que os clientes descubram o nome do estilo.
    -   Um intervalo de texto que tem vários estilos, como o título e o texto normal, deve retornar a propriedade especial de automação de interface do usuário [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) para as propriedades [**StyleID**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) e [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) . Um cliente que recebe essa resposta pode subdividir o intervalo de texto para localizar onde os estilos começam e terminam.
-   Os aplicativos podem usar uma ampla variedade de estilos para descrever objetos, mas a automação da interface do usuário representa apenas os mais comuns. Para representar atributos de estilo adicionais, como cor de borda, um provedor pode retornar uma lista de atributos adicionais na propriedade [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) . Basicamente, trata-se de um recipiente de propriedades com um conjunto de propriedades estendidas, como "BorderColor = 0xFF0000; BorderStyle = pontilhado ". Os valores das propriedades estendidas podem ser específicos do aplicativo.

## <a name="required-members-for-istylesprovider"></a>Membros necessários para **IStylesProvider**

As propriedades a seguir são necessárias para implementar a interface [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) .



| Membros necessários                                                            | Tipo de membro | Observações |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Propriedade    | Nenhum  |
| [**EstiloDePreenchimento**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Propriedade    | Nenhum  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Propriedade    | Nenhum  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Propriedade    | Nenhum  |
| [**Forma**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Propriedade    | Nenhum  |
| [**Estilo da**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Propriedade    | Nenhum  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Propriedade    | Nenhum  |



 

Este padrão de controle não tem nenhum método ou evento associado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 