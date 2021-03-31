---
title: Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)
description: Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641531"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)

Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário. Cada função de objeto inclui uma lista de métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com suporte para a função de objeto. Enquanto outros tópicos documentam métodos e propriedades de **IAccessible** com suporte para elementos de interface do usuário, este tópico lista os métodos e propriedades que você pode esperar que tenham suporte para uma função de objeto específica. Muitos dos elementos da interface do usuário que podem ter uma das funções listadas aqui normalmente são vistos em navegadores.

> [!Note]  
> Use este tópico como uma diretriz. É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado de uma função de objeto individual.

 

A tabela a seguir lista as funções de objeto adicionais às quais Oleacc.dll dá suporte.



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**\_alerta do sistema de funções \_**](/windows)                           | [**\_lista suspensa do sistema de funções \_**](/windows)       |
| [**\_aplicativo do sistema de funções \_**](/windows)               | [**\_equação do sistema de funções \_**](/windows)       |
| [**\_borda do sistema de função \_**](/windows)                         | [**\_elemento gráfico do sistema de funções \_**](/windows)         |
| [**\_BUTTONDROPDOWN do sistema de função \_**](/windows)         | [**\_HELPBALLOON do sistema de função \_**](/windows) |
| [**\_BUTTONDROPDOWNGRID do sistema de função \_**](/windows) | [**\_IPAddress do sistema de função \_**](/windows)     |
| [**\_BUTTONMENU do sistema de função \_**](/windows)                 | [**\_link do sistema de funções \_**](/windows)               |
| [**\_célula do sistema de funções \_**](/windows)                             | [**\_painel do sistema de funções \_**](/windows)               |
| [**\_caractere do sistema de funções \_**](/windows)                   | [**\_linha do sistema de função \_**](/windows)                 |
| [**\_gráfico do sistema de funções \_**](/windows)                           | [**subcabeçalho de sistema de função \_ \_**](/windows)     |
| [**\_relógio do sistema de função \_**](/windows)                           | [**separador de sistema de função \_ \_**](/windows)     |
| [**\_coluna do sistema de funções \_**](/windows)                         | [**\_som do sistema de função \_**](/windows)             |
| [**\_diagrama do sistema de funções \_**](/windows)                       | [**sistema de função \_ \_ SPLITBUTTON**](/windows) |
| [**\_discagem do sistema de função \_**](/windows)                             | [**\_tabela do sistema de funções \_**](/windows)             |
| [**\_documento do sistema de funções \_**](/windows)                     | [**espaço em branco do \_ sistema de funções \_**](/windows)   |



 

## <a name="role_system_alert"></a>\_alerta do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ alerta do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   obter \_ accName
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_application"></a>\_aplicativo do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ aplicativo do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_border"></a>\_borda do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ \_ borda do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_buttondropdown"></a>\_BUTTONDROPDOWN do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWN**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_buttondropdowngrid"></a>\_BUTTONDROPDOWNGRID do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWNGRID**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_buttonmenu"></a>\_BUTTONMENU do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONMENU**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accDefaultAction
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_cell"></a>\_célula do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ célula do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_character"></a>\_caractere do sistema de funções \_

Para obter mais informações sobre essa função, consulte [**função do \_ \_ caractere do sistema**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accDescription
-   obter \_ accFocus
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_chart"></a>\_gráfico do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ gráfico do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_clock"></a>\_relógio do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ \_ relógio do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_column"></a>\_coluna do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ coluna do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_diagram"></a>\_diagrama do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ diagrama do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_dial"></a>\_discagem do sistema de função \_

Para obter mais informações sobre essa função, consulte [**role \_ System \_ Dial**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accDefaultAction
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_document"></a>\_documento do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ documento do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_droplist"></a>\_lista suspensa do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ lista suspensa do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_equation"></a>\_equação do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ equação do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accFocus
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_graphic"></a>\_elemento gráfico do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ elemento gráfico do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_helpballoon"></a>\_HELPBALLOON do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções HELPBALLOON**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_ipaddress"></a>\_IPAddress do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ \_ IPAddress do sistema de função**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_link"></a>\_link do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ link do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accDescription
-   obter \_ accFocus
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_pane"></a>\_painel do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ painel do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_row"></a>\_linha do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ \_ linha do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDescription
-   obter \_ accFocus
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_rowheader"></a>subcabeçalho de sistema de função \_ \_

Para obter mais informações sobre essa função, consulte [**função do sistema de funções \_ \_**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDefaultAction
-   obter \_ accDescription
-   obter \_ accFocus
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState
-   obter \_ accValue

## <a name="role_system_separator"></a>separador de sistema de função \_ \_

Para obter mais informações sobre essa função, [**consulte \_ \_ separador de sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_sound"></a>\_som do sistema de função \_

Para obter mais informações sobre essa função, [**consulte \_ \_ som do sistema de função**](object-roles.md).

**Propriedades e métodos com suporte**

-   obter \_ accDescription
-   obter \_ accName
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_splitbutton"></a>sistema de função \_ \_ SPLITBUTTON

Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de função SPLITBUTTON**](object-roles.md).

**Propriedades e métodos com suporte**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obter \_ accDefaultAction
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_table"></a>\_tabela do sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ \_ tabela do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obter \_ accChild
-   obter \_ accChildCount
-   obter \_ accDescription
-   obter \_ accFocus
-   obter \_ accHelp
-   obter \_ accHelpTopic
-   obter \_ accKeyboardShortcut
-   obter \_ accName
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

## <a name="role_system_whitespace"></a>espaço em branco do \_ sistema de funções \_

Para obter mais informações sobre essa função, [**consulte \_ espaço em \_ branco do sistema de funções**](object-roles.md).

**Propriedades e métodos com suporte**

-   accLocation
-   accSelect
-   obter \_ accParent
-   obter \_ accRole
-   obter \_ accState

 

 