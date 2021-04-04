---
title: Recurso pop-up
description: Define um item de menu que pode conter itens de menu e submenus.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menus de recursos pop-up e outros recursos
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084195"
---
# <a name="popup-resource"></a><span data-ttu-id="ed39c-104">Recurso pop-up</span><span class="sxs-lookup"><span data-stu-id="ed39c-104">POPUP resource</span></span>

<span data-ttu-id="ed39c-105">Define um item de menu que pode conter itens de menu e submenus.</span><span class="sxs-lookup"><span data-stu-id="ed39c-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="ed39c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed39c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed39c-107"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="ed39c-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="ed39c-108">Cadeia de caracteres que contém o nome do menu.</span><span class="sxs-lookup"><span data-stu-id="ed39c-108">String that contains the name of the menu.</span></span> <span data-ttu-id="ed39c-109">Essa cadeia de caracteres deve ser colocada entre aspas duplas (**"**).</span><span class="sxs-lookup"><span data-stu-id="ed39c-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="ed39c-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*opção*</span><span class="sxs-lookup"><span data-stu-id="ed39c-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="ed39c-111">Esse parâmetro especifica opções de menu redefinidas que especificam a aparência do item de menu.</span><span class="sxs-lookup"><span data-stu-id="ed39c-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="ed39c-112">Esse parâmetro opcional pode ser um ou mais dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="ed39c-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="ed39c-113">Opção</span><span class="sxs-lookup"><span data-stu-id="ed39c-113">Option</span></span>           | <span data-ttu-id="ed39c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed39c-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed39c-115">**CHECK**</span><span class="sxs-lookup"><span data-stu-id="ed39c-115">**CHECKED**</span></span>      | <span data-ttu-id="ed39c-116">O item de menu tem uma marca de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="ed39c-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="ed39c-117">Essa opção não é válida para um menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="ed39c-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="ed39c-118">**ESMAECIDO**</span><span class="sxs-lookup"><span data-stu-id="ed39c-118">**GRAYED**</span></span>       | <span data-ttu-id="ed39c-119">O item de menu está inicialmente inativo e aparece no menu em cinza ou em uma tonalidade clareada da cor do texto do menu.</span><span class="sxs-lookup"><span data-stu-id="ed39c-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="ed39c-120">Esta opção não pode ser usada com a opção **inativa** .</span><span class="sxs-lookup"><span data-stu-id="ed39c-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="ed39c-121">**Ajuda**</span><span class="sxs-lookup"><span data-stu-id="ed39c-121">**HELP**</span></span>         | <span data-ttu-id="ed39c-122">Identifica um item de ajuda.</span><span class="sxs-lookup"><span data-stu-id="ed39c-122">Identifies a help item.</span></span> <span data-ttu-id="ed39c-123">O item de menu é colocado na posição mais à direita na barra de menus.</span><span class="sxs-lookup"><span data-stu-id="ed39c-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="ed39c-124">**INATIVO**</span><span class="sxs-lookup"><span data-stu-id="ed39c-124">**INACTIVE**</span></span>     | <span data-ttu-id="ed39c-125">O item de menu é exibido, mas não pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="ed39c-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="ed39c-126">Esta opção não pode ser usada com a opção **cinza** .</span><span class="sxs-lookup"><span data-stu-id="ed39c-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="ed39c-127">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="ed39c-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="ed39c-128">O mesmo que **MENUBREAK** , exceto que para menus pop-up, ele separa a nova coluna da coluna antiga com uma linha vertical.</span><span class="sxs-lookup"><span data-stu-id="ed39c-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="ed39c-129">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="ed39c-129">**MENUBREAK**</span></span>    | <span data-ttu-id="ed39c-130">Coloca o item de menu em uma nova linha para itens de barra de menus estáticos.</span><span class="sxs-lookup"><span data-stu-id="ed39c-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="ed39c-131">Para menus, ele coloca o item de menu em uma nova coluna sem linha de divisão entre as colunas.</span><span class="sxs-lookup"><span data-stu-id="ed39c-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="ed39c-132">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="ed39c-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="ed39c-133">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ed39c-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed39c-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed39c-134">Examples</span></span>

<span data-ttu-id="ed39c-135">O exemplo a seguir demonstra o uso da instrução **Popup** :</span><span class="sxs-lookup"><span data-stu-id="ed39c-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ed39c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed39c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed39c-137">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="ed39c-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="ed39c-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="ed39c-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




