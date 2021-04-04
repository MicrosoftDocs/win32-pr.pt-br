---
title: E (menus e outros recursos)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085098"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="5f1ac-103">E (menus e outros recursos)</span><span class="sxs-lookup"><span data-stu-id="5f1ac-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="5f1ac-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [i](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="5f1ac-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5f1ac-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menus vazios não são permitidos**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-106">Uma palavra-chave **end** é exibida antes de qualquer item de menu ser definido na instrução de [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="5f1ac-107">Os menus vazios não são permitidos pelo compilador de recursos do Microsoft Windows 32 (RC).</span><span class="sxs-lookup"><span data-stu-id="5f1ac-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="5f1ac-108">Certifique-se de que você não tem aspas de abertura dentro da instrução de **menu** .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**FIM esperado na caixa de diálogo**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-110">A palavra-chave **end** deve aparecer no final de uma instrução de [**diálogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="5f1ac-111">Verifique se não há aspas de abertura à esquerda da instrução anterior.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**FIM esperado no menu**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-113">A palavra-chave **end** deve aparecer no final de uma instrução de [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="5f1ac-114">Verifique se não há instruções **begin** e **end** incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Erro Creatingresource-nome**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-116">O compilador de recursos do Microsoft Windows 32 (RC) não pôde criar o recurso binário especificado (. RES).</span><span class="sxs-lookup"><span data-stu-id="5f1ac-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="5f1ac-117">Certifique-se de que ele não está sendo criado em uma unidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="5f1ac-118">Use a opção **/v** para descobrir se o arquivo está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Vírgula esperada na tabela do acelerador**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-120">O compilador de recursos do Microsoft Windows 32 (RC) requer uma vírgula entre os parâmetros *Event* e *idvalue* na instrução [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Nome de classe de controle esperado**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-122">O parâmetro de *classe* de uma instrução de [**controle**](control-control.md) na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser um dos seguintes tipos de controle: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** ou User-defined.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="5f1ac-123">Verifique se a classe está grafada corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nome de face da fonte esperado**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-125">O parâmetro de *tipo* da instrução **Font** na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser uma cadeia de caracteres entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="5f1ac-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="5f1ac-126">Esse parâmetro especifica o nome de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valor de ID esperado para MenuItem**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-128">A instrução de [**menu**](menu-resource.md) deve conter uma instrução [**MenuItem**](menuitem-statement.md) , que tem um inteiro ou uma constante simbólica no parâmetro *MenuID* .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Cadeia de menu esperada**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-130">Cada instrução [**MenuItem**](menuitem-statement.md) e [**Popup**](popup-resource.md) deve conter um parâmetro de *texto* .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="5f1ac-131">Esse parâmetro é uma cadeia de caracteres entre aspas duplas (") que especifica o nome do item de menu ou menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="5f1ac-132">Uma instrução **SEparadora MenuItem** não requer nenhuma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valor de comando numérico esperado**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-134">O compilador de recursos do Microsoft Windows (RC) estava esperando um parâmetro numérico *idvalue* na instrução [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="5f1ac-135">Certifique-se de que você usou uma instrução de [**\# definição**](-define.md) para especificar o valor e que a constante usada esteja grafada corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Constante numérica esperada na tabela de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-137">Uma constante numérica, definida em uma instrução de [**\# definição**](-define.md) , deve seguir imediatamente a palavra-chave **begin** em uma instrução [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Tamanho de ponto numérico esperado**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-139">O parâmetro de *pontos* da instrução de [**fonte**](font-statement.md) na instrução de [**diálogo**](dialog-resource.md) deve ser um valor de tamanho de ponto inteiro.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Constante de caixa de diálogo numérica esperada**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-141">Uma instrução de [**caixa de diálogo**](dialog-resource.md) requer valores inteiros para os parâmetros *x*, *y*, *Width* e *Height* .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="5f1ac-142">Verifique se esses valores, que estão incluídos após a palavra-chave da **caixa de diálogo** , não são negativos.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Cadeia de caracteres esperada em STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-144">Uma cadeia de caracteres é esperada após cada parâmetro de *stringid* numérico em uma instrução [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Cadeia de caracteres esperada ou comando acelerador de constante**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-146">O compilador de recursos do Microsoft Windows (RC) não pôde determinar qual chave estava sendo configurada para o acelerador.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="5f1ac-147">O parâmetro de *evento* na instrução [**Accelerators**](accelerators-resource.md) pode ser inválido.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**VALOR esperado, bloco ou palavra-chave END.**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-149">A estrutura [**VERSIONINFO**](versioninfo-resource.md) requer um **valor**, um **bloco** ou uma palavra-chave **end** .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Esperando número para ID**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-151">É esperado um número para o parâmetro de *ID* de uma instrução de [**controle**](control-control.md) na instrução da [**caixa de diálogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1ac-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="5f1ac-152">Verifique se você tem um número ou uma instrução de [**\# definição**](-define.md) para o identificador de controle.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Esperando cadeia de caracteres entre aspas para a chave**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-154">A cadeia de caracteres de chave após a palavra-chave de **bloco** ou **valor** deve ser colocada entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="5f1ac-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Esperando cadeia de caracteres entre aspas na classe da caixa de diálogo**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-156">O parâmetro de *classe* da instrução de [**classe**](class-statement.md) na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser um inteiro ou uma cadeia de caracteres entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="5f1ac-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="5f1ac-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Esperando cadeia de caracteres entre aspas no título da caixa de diálogo**</span><span class="sxs-lookup"><span data-stu-id="5f1ac-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="5f1ac-158">O parâmetro *CaptionText* da instrução [**Caption**](caption-statement.md) na instrução [**Dialog**](dialog-resource.md) deve ser uma cadeia de caracteres, entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="5f1ac-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




