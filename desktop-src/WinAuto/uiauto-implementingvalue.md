---
title: Padrão de controle de valor
description: Descreve as diretrizes e convenções para implementar o IValueProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automação da interface do usuário, implementando o padrão de controle de valor
- Automação da interface do usuário, padrão de controle de valor
- Automação da interface do usuário, IValueProvider
- IValueProvider
- Implementando padrões de controle de valor de automação de IU
- Padrões de controle de valor
- padrões de controle, IValueProvider
- padrões de controle, implementação do valor de automação da interface do usuário
- padrões de controle, valor
- interfaces, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366353"
---
# <a name="value-control-pattern"></a>Padrão de controle de valor

Descreve as diretrizes e convenções para implementar o [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluindo informações sobre propriedades e métodos. O padrão de controle de **valor** é usado para dar suporte a controles que têm um valor intrínseco que não abrange um intervalo e que pode ser representado como uma cadeia de caracteres.

A cadeia de caracteres de valor pode ser editável, dependendo do controle e de suas configurações. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IValueProvider**](#required-members-for-ivalueprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **valor** , observe as seguintes diretrizes e convenções:

-   Controles como um item de lista ou item de árvore devem dar suporte ao padrão de controle de **valor** se o valor de qualquer um dos itens for editável, independentemente do modo de edição atual do controle. O controle pai também deve oferecer suporte ao padrão de controle de **valor** se os itens filho forem editáveis. A imagem a seguir mostra um exemplo de um item de lista editável.

    ![ilustração mostrando item de lista editável](images/uia-valuepattern-editable-listitem.jpg)

- Os controles de edição single e multi-line devem implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para expor seu conteúdo somente leitura.
- Os controles de edição de várias linhas devem implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) se seu conteúdo puder ser alterado.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) não oferece suporte à recuperação de informações de formatação ou valores de subcadeias. Implemente [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) nesses cenários.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) deve ser implementado por controles como o controle de seleção do seletor de cores do Microsoft Word (consulte a imagem a seguir), que dá suporte ao mapeamento de cadeia de caracteres entre um valor de cor (por exemplo, "amarelo") e um valor [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.

    ![ilustração mostrando mapeamento de cadeia de caracteres de amostra de cor](images/uia-valuepattern-colorpicker.jpg)

- Um controle deve ter sua propriedade **IsEnabled** definida como **true** e sua propriedade [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) definida como **false** antes de permitir uma chamada para [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).

## <a name="required-members-for-ivalueprovider"></a>Membros necessários para **IValueProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .



| Membros necessários                                       | Tipo de membro | Observações |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Propriedade    | Nenhum  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Propriedade    | Nenhum  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 