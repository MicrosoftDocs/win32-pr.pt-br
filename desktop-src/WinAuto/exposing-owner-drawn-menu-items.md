---
title: Expondo Owner-Drawn itens de menu
description: Expondo Owner-Drawn itens de menu
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498754"
---
# <a name="exposing-owner-drawn-menu-items"></a>Expondo Owner-Drawn itens de menu

Os desenvolvedores de aplicativos podem usar a estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para expor os nomes dos itens de menu desenhados pelo proprietário. Ao associar essa estrutura com os dados do item de menu desenhado pelo proprietário, você não precisa expor os itens de menu com o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Ao criar um menu desenhado pelo proprietário, defina uma classe ou estrutura para os dados do item de menu desenhado pelo proprietário e crie instâncias dessa classe para cada item de menu. Passe um ponteiro para os dados do item ao adicionar itens ao menu.

Para expor os nomes dos itens de menu, a estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) deve ser o primeiro membro da estrutura que define os dados de item específicos do aplicativo, conforme mostrado no exemplo a seguir:


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



A estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) não pode ser um membro em uma classe que contém funções virtuais. Quando o código é compilado, o primeiro membro da classe é sempre um ponteiro gerado pelo compilador para uma tabela das funções virtuais. Para contornar esse problema, crie uma estrutura de dados de item que contenha **MSAAMENUINFO** como o primeiro membro. O segundo membro é um ponteiro para uma instância da classe que define os dados desenhados pelo proprietário. O exemplo a seguir demonstra essa técnica.


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



Ao adicionar itens ao menu, passe um ponteiro para uma instância da estrutura que contém [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para expor os nomes dos itens de menu.

 

 




