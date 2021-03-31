---
title: Padrão de controle LegacyIAccessible
description: Descreve as diretrizes e convenções para usar o ILegacyIAccessibleProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Automação da interface do usuário, implementando o padrão de controle LegacyIAccessible
- Automação da interface do usuário, padrão de controle LegacyIAccessible
- Automação da interface do usuário, ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- Implementando padrões de controle LegacyIAccessible de automação da interface do usuário
- Padrões de controle LegacyIAccessible
- padrões de controle, ILegacyIAccessibleProvider
- padrões de controle, implementando a automação da interface do usuário LegacyIAccessible
- padrões de controle, LegacyIAccessible
- interfaces, ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636460"
---
# <a name="legacyiaccessible-control-pattern"></a>Padrão de controle LegacyIAccessible

Descreve as diretrizes e convenções para usar o [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), incluindo informações sobre propriedades, métodos e eventos. O padrão de controle **LegacyIAccessible** é suportado pelo Microsoft acessibilidade ativa para o proxy de automação da interface do usuário da Microsoft.

Provedores de aplicativo e controle nunca implementam a interface [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) .

O padrão de controle **LegacyIAccessible** expõe a interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) aos clientes de automação da interface do usuário, permitindo que eles acessem a implementação base do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para determinados elementos da interface do usuário. No entanto, o **IUIAutomationLegacyIAccessiblePattern** não oferece suporte a métodos obsoletos ou que são redundantes com os recursos de automação da interface do usuário.

Este tópico contém as seguintes seções:

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros do padrão de controle **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Nenhum aplicativo ou controle implementa [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). A estrutura de automação da interface do usuário fornece automaticamente a implementação do provedor para um Microsoft Acessibilidade Ativa Server nativo.

O padrão de controle **LegacyIAccessible** não está disponível para controles baseados na automação da interface do usuário.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Membros do padrão de controle **LegacyIAccessible**

As propriedades, os métodos e os eventos a seguir são membros do padrão de controle **LegacyIAccessible** . As observações são para clientes de automação da interface do usuário.



| Membros                                                                        | Tipo de membro | Observações                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildID**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Propriedade    | Retorna **filhaid \_ própria** (0) para um objeto não filho.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Propriedade    | Nenhum                                                                                                                                 |
| [**Descrição**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Propriedade    | Nenhum                                                                                                                                 |
| [**Ajuda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Propriedade    | Nenhum                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Propriedade    | Nenhum                                                                                                                                 |
| [**Nome**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Propriedade    | Nenhum                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Propriedade    | Use a função [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar a cadeia de caracteres localizada.                                                    |
| [**Getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Método      | Recupera um ponteiro de interface [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) .                                |
| [**Estado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Propriedade    | Use a função [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar a cadeia de caracteres localizada.                                                  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Propriedade    | Nenhum                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Método      | Nenhum                                                                                                                                 |
| [**Getiaccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Método      | Nenhum                                                                                                                                 |
| [**Não**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Método      | O sinalizador de seleção é um valor de **SELFLAG** da Microsoft acessibilidade ativa. Para obter mais informações, consulte [constantes SELFLAG](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Método      | Nenhum                                                                                                                                 |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




