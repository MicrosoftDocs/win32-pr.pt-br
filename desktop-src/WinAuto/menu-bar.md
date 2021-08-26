---
title: Barra de menus (Referência de elemento de interface do usuário MSAA)
description: Uma barra de menus é a área de uma janela imediatamente abaixo da barra de título que contém itens de menu, como Arquivo, Editar, Janela e Ajuda.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1212ba3c56673ab638e5aeedcc0ce20aea68dda2ad55e0904906d9f809c234ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998406"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra de menus (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve objetos **da Barra de Menus** para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **da Barra de Menus** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Uma barra de menus é a área de uma janela imediatamente abaixo da barra de título que contém itens de menu, como **Arquivo**, **Editar**, **Janela** e **Ajuda**. Microsoft Active Accessibility também cria um objeto de barra de menus para um menu do sistema, que é o menu no canto superior esquerdo da barra de título e contém itens de menu como **Restaurar,** Mover **,** **Tamanho,** **Minimizar** e Maximizar **.**

> [!Note]  
> Como os controles da barra de menus não recebem foco, os métodos [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) não têm suporte para esse controle.

 

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles da barra de menus suportam os seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Os controles da barra de menus suportam as seguintes propriedades [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera o [**IDispatch para**](idispatch-interface.md) o item de menu especificado. As IDs filho para os itens de menu são numeradas sequencialmente da esquerda para a direita, começando com uma.                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A **propriedade ChildCount** é o número de itens de menu na barra de menus. A **propriedade ChildCount** para um menu do sistema é uma.                                                                                                                                                                                                                                                   |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | A **propriedade Description** de uma barra de menus é "Contém comandos para manipular a exibição ou o documento atual". A **propriedade Description** de um menu do sistema é "Contém comandos para manipular a janela".                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A **propriedade KeyboardShortcut** para uma barra de menus abaixo da barra de título é "Alt". A **propriedade KeyboardShortcut** para um menu do sistema é "Alt+Espaço".                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A **propriedade Nome** de uma barra de menus abaixo da barra de título é "Aplicativo". A **propriedade Nome** de um menu do sistema é "Sistema".                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A **propriedade Role** é ROLE SYSTEM [**\_ \_ MENUBAR**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM FOCUSED STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

O sistema dispara mais de um evento [**\_ \_ MENUSTART**](event-constants.md) do SISTEMA DE EVENTOS que nem sempre tem um evento [**\_ \_ MENUEND do SISTEMA DE**](event-constants.md) EVENTOS correspondente. Além disso, o sistema não dispara os eventos [**MENU DO SISTEMA DE \_ \_ EVENTOSPOPUPSTART**](event-constants.md) e [**MENU DO SISTEMA DE \_ \_ EVENTOSPOPUPEND**](event-constants.md) de forma consistente. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menu Item**](menu-item.md)
</dt> <dt>

[**Pop-up Menu**](pop-up-menu.md)
</dt> </dl>

 

 





