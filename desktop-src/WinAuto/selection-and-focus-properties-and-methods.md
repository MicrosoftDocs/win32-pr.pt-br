---
title: Propriedades e métodos de seleção e foco
description: Como muitos elementos em aplicativos executados em sistemas operacionais Microsoft Windows, os objetos acessíveis selecionam e recebem o foco do teclado. Esses atributos permitem que os usuários interajam com os elementos do aplicativo, alteram valores e os manipulam de outra forma.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641382"
---
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="06062-104">Propriedades e métodos de seleção e foco</span><span class="sxs-lookup"><span data-stu-id="06062-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="06062-105">Como muitos elementos em aplicativos executados em sistemas operacionais Microsoft Windows, os objetos acessíveis *selecionam* e recebem o *foco* do teclado.</span><span class="sxs-lookup"><span data-stu-id="06062-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="06062-106">Esses atributos permitem que os usuários interajam com os elementos do aplicativo, alteram valores e os manipulam de outra forma.</span><span class="sxs-lookup"><span data-stu-id="06062-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="06062-107">Há algumas diferenças importantes entre a seleção de objetos e o foco do objeto:</span><span class="sxs-lookup"><span data-stu-id="06062-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="06062-108">Um objeto focalizado é um objeto em todo o sistema operacional que recebe entrada de teclado.</span><span class="sxs-lookup"><span data-stu-id="06062-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="06062-109">O objeto com o foco do teclado é a janela ativa ou um objeto filho da janela ativa.</span><span class="sxs-lookup"><span data-stu-id="06062-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="06062-110">Um objeto selecionado está marcado para participar de algum tipo de operação de grupo.</span><span class="sxs-lookup"><span data-stu-id="06062-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="06062-111">Por exemplo, um usuário pode selecionar vários itens em um controle de exibição de lista, mas o foco é fornecido somente a um objeto no sistema de cada vez.</span><span class="sxs-lookup"><span data-stu-id="06062-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="06062-112">Observe que os itens focados são de uma seleção de itens.</span><span class="sxs-lookup"><span data-stu-id="06062-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="06062-113">Os clientes determinam se um determinado objeto acessível ou elemento filho tem o foco chamando [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span><span class="sxs-lookup"><span data-stu-id="06062-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="06062-114">Os clientes determinam se um objeto está selecionado ou quais filhos dentro de um objeto acessível são selecionados, chamando [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span><span class="sxs-lookup"><span data-stu-id="06062-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="06062-115">Para objetos como controles de exibição de lista em que mais de um filho é selecionado, o objeto pai deve dar suporte à interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , que permite aos clientes enumerar os filhos selecionados.</span><span class="sxs-lookup"><span data-stu-id="06062-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="06062-116">Eventos disparados em menus</span><span class="sxs-lookup"><span data-stu-id="06062-116">Events Triggered in Menus</span></span>

<span data-ttu-id="06062-117">O Microsoft Acessibilidade Ativa expõe os menus padrão criados com as APIs de menu e os arquivos de recursos do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="06062-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="06062-118">Para ser consistente com menus padrão, os servidores com menus personalizados disparam o [**\_ \_ foco do objeto de evento**](event-constants.md), não a [**\_ \_ seleção de objeto de evento**](event-constants.md), quando um usuário realça um item de menu.</span><span class="sxs-lookup"><span data-stu-id="06062-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="06062-119">O Microsoft Acessibilidade Ativa não oferece suporte à seleção do texto contido em controles editar e Rich Edit porque o texto é exposto como uma única cadeia de caracteres na propriedade [**Value**](value-property.md) para esses controles.</span><span class="sxs-lookup"><span data-stu-id="06062-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="06062-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="06062-120">In this section</span></span>

-   [<span data-ttu-id="06062-121">Selecionando objetos filho</span><span class="sxs-lookup"><span data-stu-id="06062-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 