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
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="82ccb-103">Expondo Owner-Drawn itens de menu</span><span class="sxs-lookup"><span data-stu-id="82ccb-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="82ccb-104">Os desenvolvedores de aplicativos podem usar a estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para expor os nomes dos itens de menu desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="82ccb-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="82ccb-105">Ao associar essa estrutura com os dados do item de menu desenhado pelo proprietário, você não precisa expor os itens de menu com o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="82ccb-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="82ccb-106">Ao criar um menu desenhado pelo proprietário, defina uma classe ou estrutura para os dados do item de menu desenhado pelo proprietário e crie instâncias dessa classe para cada item de menu.</span><span class="sxs-lookup"><span data-stu-id="82ccb-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="82ccb-107">Passe um ponteiro para os dados do item ao adicionar itens ao menu.</span><span class="sxs-lookup"><span data-stu-id="82ccb-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="82ccb-108">Para expor os nomes dos itens de menu, a estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) deve ser o primeiro membro da estrutura que define os dados de item específicos do aplicativo, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="82ccb-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


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



<span data-ttu-id="82ccb-109">A estrutura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) não pode ser um membro em uma classe que contém funções virtuais.</span><span class="sxs-lookup"><span data-stu-id="82ccb-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="82ccb-110">Quando o código é compilado, o primeiro membro da classe é sempre um ponteiro gerado pelo compilador para uma tabela das funções virtuais.</span><span class="sxs-lookup"><span data-stu-id="82ccb-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="82ccb-111">Para contornar esse problema, crie uma estrutura de dados de item que contenha **MSAAMENUINFO** como o primeiro membro.</span><span class="sxs-lookup"><span data-stu-id="82ccb-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="82ccb-112">O segundo membro é um ponteiro para uma instância da classe que define os dados desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="82ccb-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="82ccb-113">O exemplo a seguir demonstra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="82ccb-113">The following example demonstrates this technique.</span></span>


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



<span data-ttu-id="82ccb-114">Ao adicionar itens ao menu, passe um ponteiro para uma instância da estrutura que contém [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) para expor os nomes dos itens de menu.</span><span class="sxs-lookup"><span data-stu-id="82ccb-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




