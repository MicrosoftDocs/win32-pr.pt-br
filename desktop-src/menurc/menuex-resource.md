---
title: Recurso MENUEX
description: Define o conteúdo de um recurso de menu. | Recurso MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menus de recursos do MENUEX e outros recursos
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105764183"
---
# <a name="menuex-resource"></a><span data-ttu-id="be965-105">Recurso MENUEX</span><span class="sxs-lookup"><span data-stu-id="be965-105">MENUEX resource</span></span>

<span data-ttu-id="be965-106">Define o conteúdo de um recurso de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="be965-107">Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be965-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="be965-108">Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus de uma lista de itens de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="be965-109">Ele também define o seguinte:</span><span class="sxs-lookup"><span data-stu-id="be965-109">It also defines the following:</span></span>

-   <span data-ttu-id="be965-110">Identificadores de ajuda em menus.</span><span class="sxs-lookup"><span data-stu-id="be965-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="be965-111">Identificadores em menus.</span><span class="sxs-lookup"><span data-stu-id="be965-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="be965-112">Uso dos sinalizadores de tipo **MFT \_ \** _ e sinalizadores de estado _*MFS \_ \*\*_ .</span><span class="sxs-lookup"><span data-stu-id="be965-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="be965-113">Para obter mais informações sobre esses sinalizadores, consulte a estrutura [_ *MENUITEMINFO* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="be965-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="be965-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be965-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be965-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="be965-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="be965-116">Define um item de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="be965-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*Texto*</span><span class="sxs-lookup"><span data-stu-id="be965-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="be965-118">Cadeia de caracteres que contém o texto do item de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-118">String containing the text for the menu item.</span></span> <span data-ttu-id="be965-119">Para obter mais informações, consulte [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="be965-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be965-120"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="be965-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="be965-121">Expressão numérica que indica o identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="be965-122"><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="be965-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="be965-123">Expressão numérica que indica o tipo do item de menu para usar os valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="be965-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="be965-124"><span id="state"></span><span id="STATE"></span>*status*</span><span class="sxs-lookup"><span data-stu-id="be965-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="be965-125">Expressão numérica que indica o estado do item de menu para usar os valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução em seu. Arquivo RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="be965-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="be965-126"><span id="POPUP"></span><span id="popup"></span>[**POP-up**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="be965-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="be965-127">Define um item de menu que tem um submenu associado a ele.</span><span class="sxs-lookup"><span data-stu-id="be965-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="be965-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*Texto*</span><span class="sxs-lookup"><span data-stu-id="be965-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="be965-129">Cadeia de caracteres que contém o texto do item de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="be965-130"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="be965-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="be965-131">Expressão numérica que indica o identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="be965-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="be965-132"><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="be965-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="be965-133">Expressão numérica que indica o tipo do item de menu para usar os valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução em seu. Arquivo RC:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="be965-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="be965-134"><span id="state"></span><span id="STATE"></span>*status*</span><span class="sxs-lookup"><span data-stu-id="be965-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="be965-135">Expressão numérica que indica o estado do item de menu para usar os valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="be965-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="be965-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="be965-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="be965-137">Expressão numérica que indica o identificador usado para identificar o menu durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="be965-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="be965-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span><span class="sxs-lookup"><span data-stu-id="be965-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="be965-139">Contém qualquer combinação das instruções [**MenuItem**](menuitem-statement.md) e [**Popup**](popup-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="be965-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="be965-140">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="be965-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="be965-141">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="be965-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be965-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="be965-142">Remarks</span></span>

<span data-ttu-id="be965-143">As operações aritméticas e booleanas válidas que podem estar contidas em qualquer uma das expressões numéricas nas instruções de **MENUEX** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="be965-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="be965-144">Adicionar (' + ')</span><span class="sxs-lookup"><span data-stu-id="be965-144">Add ('+')</span></span>
-   <span data-ttu-id="be965-145">Subtrair ('-')</span><span class="sxs-lookup"><span data-stu-id="be965-145">Subtract ('-')</span></span>
-   <span data-ttu-id="be965-146">Menos unário ('-')</span><span class="sxs-lookup"><span data-stu-id="be965-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="be965-147">Não unário (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="be965-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="be965-148">E (' & ')</span><span class="sxs-lookup"><span data-stu-id="be965-148">AND ('&')</span></span>
-   <span data-ttu-id="be965-149">OU (' \| ')</span><span class="sxs-lookup"><span data-stu-id="be965-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="be965-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="be965-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be965-151">Uso de Menus</span><span class="sxs-lookup"><span data-stu-id="be965-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="be965-152">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="be965-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-153">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="be965-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="be965-154">**'**</span><span class="sxs-lookup"><span data-stu-id="be965-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-155">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="be965-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="be965-156">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="be965-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="be965-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="be965-158">**POP-up**</span><span class="sxs-lookup"><span data-stu-id="be965-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="be965-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="be965-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="be965-161">**Versão**</span><span class="sxs-lookup"><span data-stu-id="be965-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
