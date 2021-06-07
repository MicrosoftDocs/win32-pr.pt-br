---
title: Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)
description: Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443997"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)

Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário. Cada função de objeto inclui uma lista de métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com suporte para a função de objeto. Enquanto outros tópicos documentam métodos e propriedades de **IAccessible** com suporte para elementos de interface do usuário, este tópico lista os métodos e propriedades que você pode esperar que tenham suporte para uma função de objeto específica. Muitos dos elementos da interface do usuário que podem ter uma das funções listadas aqui normalmente são vistos em navegadores.

> [!Note]  
> Use este tópico como uma diretriz. É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado de uma função de objeto individual.

 

A tabela a seguir lista as funções de objeto adicionais às quais Oleacc.dll dá suporte.



| &nbsp; |  &nbsp; |
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
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttonmenu"></a>BOTÃO \_ DO SISTEMA DE \_ FUNÇÃOMENU

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).

**Propriedades e métodos com suporte**

-   Accdodefaultaction
-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_cell"></a>CÉLULA \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   Accselect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_character"></a>CARACTERE \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_chart"></a>GRÁFICO \_ DO SISTEMA DE \_ FUNÇÕES

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_clock"></a>RELÓGIO \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_column"></a>COLUNA \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   Accselect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_diagram"></a>DIAGRAMA \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_dial"></a>ROLE \_ SYSTEM \_ DIAL

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).

**Propriedades e métodos com suporte**

-   Accdodefaultaction
-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_document"></a>DOCUMENTO DO \_ SISTEMA \_ DE FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   Accselect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_droplist"></a>LISTA \_ DE DROPLIST DO \_ SISTEMA DE FUNÇÕES

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).

**Propriedades e métodos com suporte**

-   Accdodefaultaction
-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_equation"></a>EQUAÇÃO \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_graphic"></a>GRÁFICO \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_helpballoon"></a>ROLE \_ SYSTEM \_ HELPBALLBALLBALLBALL

Para obter mais informações sobre essa função, [**consulte ROLE \_ SYSTEM \_ HELPBALLBALLBALL .**](object-roles.md)

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_ipaddress"></a>ROLE \_ SYSTEM \_ IPADDRESS

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_link"></a>\_LINK DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).

**Propriedades e métodos com suporte**

-   Accdodefaultaction
-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_pane"></a>PAINEL \_ SISTEMA \_ DE FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_row"></a>LINHA \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   Accselect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_rowheader"></a>\_ROWHEADER DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, [**consulte ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   Accnavigate
-   Accselect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_separator"></a>SEPARADOR \_ DO \_ SISTEMA DE FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).

**Propriedades e métodos com suporte**

-   Acchittest
-   Acclocation
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_sound"></a>SOM \_ DO SISTEMA DE \_ FUNÇÃO

Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).

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

 

 