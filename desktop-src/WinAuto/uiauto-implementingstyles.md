---
title: Padrão de controle estilos
description: Descreve diretrizes e convenções para implementar IStylesProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Estilos é usado para descrever um elemento de interface do usuário que tem um estilo específico, cor de preenchimento, padrão de preenchimento ou forma.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle Estilos
- Automação da Interface do Usuário, padrão de controle Estilos
- Automação da Interface do Usuário,IStylesProvider
- IStylesProvider
- implementando o Automação da Interface do Usuário de controle estilos
- Padrão de controle de estilos
- padrões de controle, IStylesProvider
- padrões de controle, implementando Automação da Interface do Usuário Estilos
- padrões de controle, Estilos
- interfaces,IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e52a6829e592cc659d5ce47b51a09b6d8910d4bd2c41a1e03c9b661d027fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324084"
---
# <a name="styles-control-pattern"></a>Padrão de controle estilos

Descreve diretrizes e convenções para implementar [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), incluindo informações sobre propriedades e métodos. O **padrão de** controle Estilos é usado para descrever um elemento de interface do usuário que tem um estilo específico, cor de preenchimento, padrão de preenchimento ou forma.

O **padrão de** controle Estilos é especialmente útil para descrever elementos em um documento, que frequentemente têm esses estilos. Os estilos normalmente carregam informações úteis para clientes com deficiências; por exemplo, um estilo pode descrever uma determinada cadeia de caracteres como o título de um documento ou um determinado objeto de fluxograma como um losango ou um círculo. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IStylesProvider**](#required-members-for-istylesprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle Estilos,** observe as seguintes diretrizes e convenções:

-   O arquivo de header UIAutomationClient.h define um conjunto de valores constantes nomeados usados para identificar vários estilos comuns. Para obter mais informações, consulte [**Identificadores de estilo**](uiauto-style-identifiers.md).
-   Se você usar [**StyleId \_ Custom**](uiauto-style-identifiers.md), deverá implementar a propriedade [**IStylesProvider::StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que os clientes descubram o nome do estilo. Você não precisa implementar a propriedade **StyleName** para um estilo padrão porque o Microsoft Automação da Interface do Usuário fornece um nome padrão, mas pode implementá-la se precisar substituir o nome padrão.
-   As outras propriedades no padrão **Estilos** são opcionais; O provedor pode retornar [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) para uma propriedade que não tem suporte.
-   Os estilos em um intervalo de texto podem ser representados por meio dos seguintes atributos de texto:
    -   Ao responder a uma solicitação para o atributo de texto [**StyleId,**](uiauto-textattribute-ids.md) o intervalo de texto deve retornar um dos identificadores de estilo descritos em [**Identificadores de Estilo**](uiauto-style-identifiers.md).
    -   Se [**StyleId \_ Custom for**](uiauto-style-identifiers.md) usado, o intervalo de texto deverá retornar um valor de cadeia de caracteres para o atributo de texto [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que os clientes descubram o nome de estilo.
    -   Um intervalo de texto que tem vários estilos, como título e texto normal, deve retornar a propriedade especial Automação da Interface do Usuário [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) para as propriedades [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) e [**StyleName.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) Um cliente que recebe essa resposta pode subdividir o intervalo de texto para descobrir onde os estilos começam e terminam.
-   Os aplicativos podem usar uma ampla variedade de estilos para descrever objetos, mas Automação da Interface do Usuário representa apenas os mais comuns. Para representar atributos de estilo adicionais, como a cor da borda, um provedor pode retornar uma lista de atributos adicionais na propriedade [**ExtendedProperties.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) Isso é basicamente um pacote de propriedades com um conjunto de propriedades estendidas, como "BorderColor=0xFF0000; BorderStyle=dotted". Os valores das propriedades estendidas podem ser específicos do aplicativo.

## <a name="required-members-for-istylesprovider"></a>Membros necessários para **IStylesProvider**

As propriedades a seguir são necessárias para implementar a interface [**IStylesProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)



| Membros necessários                                                            | Tipo de membro | Observações |
|-----------------------------------------------------------------------------|-------------|-------|
| [**Extendedproperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Propriedade    | Nenhum  |
| [**Fillcolor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Propriedade    | Nenhum  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Propriedade    | Nenhum  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Propriedade    | Nenhum  |
| [**Forma**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Propriedade    | Nenhum  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Propriedade    | Nenhum  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Propriedade    | Nenhum  |



 

Esse padrão de controle não tem métodos ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 