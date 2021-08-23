---
title: Item de menu (referência de elemento de interface do usuário do MSAA)
description: Um item de menu representa um item específico em uma barra de menus ou em um menu pop-up.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b90162f386314ac495ed138ccf4d180d2f53b8b1e6126287c79a1d75d40be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644496"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Item de menu (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos de **item de menu** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **item de menu** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um item de menu representa um item específico em uma barra de menus ou em um menu pop-up. Por exemplo, o Microsoft Acessibilidade Ativa cria um objeto de item de menu para o menu **arquivo** na barra de menus. Da mesma forma, o Microsoft Acessibilidade Ativa cria um objeto de item de menu para o item de menu **aberto** no menu pop-up de **arquivo** .

O nome da classe da janela para um item de menu é " \# 32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um item de menu dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Para itens de menu da barra de menus, o [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) exibe ou fecha o menu dependendo do estado do menu. Para itens de menu de um menu pop-up, **accDoDefaultAction** clica no item de menu para executar o comando de menu. |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um item de menu dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera a interface [**IDispatch**](idispatch-interface.md) para o objeto de menu pop-up deste item.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é uma para itens de menu que exibem um menu ou submenu; caso contrário, a propriedade **ChildCount** será zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | A propriedade **DefaultAction** para itens de menu que exibem um menu ou submenu é "Open" ou "Close", dependendo do estado do menu. A propriedade **DefaultAction** para todos os outros itens de menu é "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a chave de acesso do item de menu, que é o caractere sublinhado no texto do nome do item de menu. Por exemplo, a propriedade **KeyboardShortcut** para o item de menu arquivo é "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é igual ao nome do item de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é a barra de menus ou o menu pop-up que contém o item de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é o [**sistema de função \_ \_ MenuItem**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade **State** é um [**sistema de estado \_ \_ invisível**](object-state-constants.md) ou uma combinação de um ou mais dos seguintes valores: [**estado do \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ verificado**](object-state-constants.md) sistema de estado \| [**\_ \_ padrão**](object-state-constants.md) System \| [**\_ \_ HOTTRACKED**](object-state-constants.md) estado sistema estado do sistema \| [**\_ \_ foco**](object-state-constants.md) \| [**\_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

-   Quando usado em um item de menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) retorna S \_ OK, mas falha ao executar a ação se o caractere usado na chave de acesso for?,!, @ ou qualquer outro caractere que exija a tecla Shift ou outra tecla modificadora. Isso também ocorre em teclados internacionais com um caractere de chave de acesso que exige que a tecla ALT GR seja pressionada.
-   O método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) com [**SELFLAG \_ TAKEFOCUS**](selflag.md) não faz com que um item de menu abra ou feche um menu pop-up. Os clientes usam o método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para abrir ou fechar um menu pop-up.
-   Um item da barra de menus que não exibe um menu pop-up retorna "Application" para a propriedade **Name** em vez do nome do item de menu.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menus**](menu-bar.md)
</dt> <dt>

[**Menu pop-up**](pop-up-menu.md)
</dt> </dl>

 

 





