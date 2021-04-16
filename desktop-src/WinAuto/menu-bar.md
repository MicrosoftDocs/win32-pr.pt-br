---
title: Barra de menus (referência de elemento de interface do usuário do MSAA)
description: Uma barra de menus é a área de uma janela imediatamente abaixo da barra de título que contém itens de menu, como arquivo, editar, janela e ajuda.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498702"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra de menus (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **barra de menu** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **barra de menus** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Uma barra de menus é a área de uma janela imediatamente abaixo da barra de título que contém itens de menu, como **arquivo**, **Editar**, **janela** e **ajuda**. O Microsoft Acessibilidade Ativa também cria um objeto de barra de menus para um menu do sistema, que é o menu no canto superior esquerdo da barra de título e contém itens de menu, como **restaurar**, **mover**, **dimensionar**, **minimizar** e **maximizar**.

> [!Note]  
> Como os controles de barra de menus não recebem foco, os métodos [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e [**Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) não têm suporte para esse controle.

 

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de barra de menus dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de barra de menus dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera o [**IDispatch**](idispatch-interface.md) para o item de menu especificado. As IDs filho dos itens de menu são numeradas em sequência da esquerda para a direita, começando com uma.                                                                                                                                                                                             |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é o número de itens de menu na barra de menus. A propriedade **ChildCount** para um menu do sistema é uma.                                                                                                                                                                                                                                                   |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | A propriedade **Descrição** de uma barra de menus é "contém comandos para manipular a exibição ou o documento atual". A propriedade **Description** de um menu do sistema é "contém comandos para manipular a janela".                                                                                                                                                                   |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** de uma barra de menus abaixo da barra de título é "Alt". A propriedade **KeyboardShortcut** para um menu do sistema é "Alt + Space".                                                                                                                                                                                                                             |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** de uma barra de menus abaixo da barra de título é "Application". A propriedade **Name** de um menu do sistema é "System".                                                                                                                                                                                                                                                |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**a \_ \_ MenuBar do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): estado do sistema invisíveis sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

O sistema dispara mais de um [**evento \_ \_ MENUSTART do sistema de eventos**](event-constants.md) que nem sempre tem um evento [**\_ \_ MENUEND do sistema de eventos**](event-constants.md) correspondente. Além disso, o sistema não aciona os eventos do sistema de eventos [**\_ \_ MENUPOPUPSTART**](event-constants.md) e do sistema de [**eventos \_ \_ MENUPOPUPEND**](event-constants.md) de forma consistente. Esse é um problema conhecido e está sendo resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Item de menu**](menu-item.md)
</dt> <dt>

[**Menu pop-up**](pop-up-menu.md)
</dt> </dl>

 

 





