---
title: Propriedade Value
description: A propriedade Value fornece uma representação textual das informações visuais contidas em um objeto. Nem todos os objetos dão suporte à propriedade Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292245"
---
# <a name="value-property"></a><span data-ttu-id="42d2b-104">Propriedade Value</span><span class="sxs-lookup"><span data-stu-id="42d2b-104">Value Property</span></span>

<span data-ttu-id="42d2b-105">A propriedade **Value** fornece uma representação textual das informações visuais contidas em um objeto.</span><span class="sxs-lookup"><span data-stu-id="42d2b-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="42d2b-106">Nem todos os objetos dão suporte à propriedade **Value** .</span><span class="sxs-lookup"><span data-stu-id="42d2b-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="42d2b-107">A propriedade **Value** é recuperada chamando [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="42d2b-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="42d2b-108">A propriedade **Value** informa ao cliente sobre as informações visuais contidas em um objeto.</span><span class="sxs-lookup"><span data-stu-id="42d2b-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="42d2b-109">Por exemplo, um valor de controle de edição é o texto que ele contém, enquanto que um item de menu não tem nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="42d2b-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="42d2b-110">Fornecendo informações hierárquicas</span><span class="sxs-lookup"><span data-stu-id="42d2b-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="42d2b-111">A propriedade **Value** fornece informações hierárquicas em casos como um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="42d2b-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="42d2b-112">Embora o objeto pai no controle de exibição de árvore não forneça informações na propriedade **Value** , cada item dentro do controle tem um valor de base zero que representa seu nível dentro da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="42d2b-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="42d2b-113">Itens de nível superior têm um valor de zero, itens de segundo nível têm um valor de um, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="42d2b-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




