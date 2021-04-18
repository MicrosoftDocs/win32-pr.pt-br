---
title: Instrução MENUITEM
description: Define um item de menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menus de instrução MENUITEM e outros recursos
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105759016"
---
# <a name="menuitem-statement"></a><span data-ttu-id="3801b-104">Instrução MENUITEM</span><span class="sxs-lookup"><span data-stu-id="3801b-104">MENUITEM statement</span></span>

<span data-ttu-id="3801b-105">Define um item de menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="3801b-106"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="3801b-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="3801b-107">O nome do item de menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-107">The name of the menu item.</span></span>

<span data-ttu-id="3801b-108">A cadeia de caracteres pode conter os caracteres de escape **\\ t** e **\\ a**.</span><span class="sxs-lookup"><span data-stu-id="3801b-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="3801b-109">O caractere **\\ t** insere uma guia na cadeia de caracteres e é usado para alinhar o texto em colunas.</span><span class="sxs-lookup"><span data-stu-id="3801b-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="3801b-110">Os caracteres de tabulação devem ser usados somente em menus, não em barras de menus.</span><span class="sxs-lookup"><span data-stu-id="3801b-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="3801b-111">(Para obter informações sobre menus, consulte [**recurso pop-up**](popup-resource.md).) O caractere **\\ um** alinha todo o texto que o segue à direita até a barra de menus ou menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="3801b-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="3801b-112"><span id="result"></span><span id="RESULT"></span>*disso*</span><span class="sxs-lookup"><span data-stu-id="3801b-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="3801b-113">Um número que especifica o resultado gerado quando o usuário seleciona o item de menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="3801b-114">Esse parâmetro usa um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="3801b-114">This parameter takes an integer value.</span></span> <span data-ttu-id="3801b-115">Menu – os resultados do item são sempre inteiros; Quando o usuário clica no nome do item de menu, o resultado é enviado para a janela que possui o menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="3801b-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*opção*</span><span class="sxs-lookup"><span data-stu-id="3801b-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="3801b-117">A aparência do item de menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-117">The appearance of the menu item.</span></span> <span data-ttu-id="3801b-118">Esse parâmetro opcional usa uma ou mais das seguintes opções de menu redefinida, separadas por vírgulas ou espaços.</span><span class="sxs-lookup"><span data-stu-id="3801b-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="3801b-119">Opção</span><span class="sxs-lookup"><span data-stu-id="3801b-119">Option</span></span>           | <span data-ttu-id="3801b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="3801b-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3801b-121">**CHECK**</span><span class="sxs-lookup"><span data-stu-id="3801b-121">**CHECKED**</span></span>      | <span data-ttu-id="3801b-122">O item de menu tem uma marca de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="3801b-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="3801b-123">**ESMAECIDO**</span><span class="sxs-lookup"><span data-stu-id="3801b-123">**GRAYED**</span></span>       | <span data-ttu-id="3801b-124">O item de menu está inicialmente inativo e aparece no menu em cinza ou em uma tonalidade clareada da cor do texto do menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="3801b-125">Esta opção não pode ser usada com a opção **inativa** .</span><span class="sxs-lookup"><span data-stu-id="3801b-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="3801b-126">**Ajuda**</span><span class="sxs-lookup"><span data-stu-id="3801b-126">**HELP**</span></span>         | <span data-ttu-id="3801b-127">Identifica um item de ajuda.</span><span class="sxs-lookup"><span data-stu-id="3801b-127">Identifies a help item.</span></span> <span data-ttu-id="3801b-128">Essa opção não tem efeito sobre a aparência do item de menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="3801b-129">**INATIVO**</span><span class="sxs-lookup"><span data-stu-id="3801b-129">**INACTIVE**</span></span>     | <span data-ttu-id="3801b-130">O item de menu é exibido, mas não pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="3801b-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="3801b-131">Esta opção não pode ser usada com a opção **cinza** .</span><span class="sxs-lookup"><span data-stu-id="3801b-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="3801b-132">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="3801b-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="3801b-133">O mesmo que **MENUBREAK** , exceto que para menus pop-up, ele separa a nova coluna da coluna antiga com uma linha vertical.</span><span class="sxs-lookup"><span data-stu-id="3801b-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="3801b-134">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="3801b-134">**MENUBREAK**</span></span>    | <span data-ttu-id="3801b-135">Coloca o item de menu em uma nova linha para itens de barra de menus estáticos.</span><span class="sxs-lookup"><span data-stu-id="3801b-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="3801b-136">Para menus, ele coloca o item de menu em uma nova coluna sem linha de divisão entre as colunas.</span><span class="sxs-lookup"><span data-stu-id="3801b-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="3801b-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARADOR MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="3801b-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="3801b-138">O formulário **SEparador MenuItem** da instrução **MenuItem** cria um item de menu inativo que serve como uma barra de divisão entre dois itens de menu ativos em um menu.</span><span class="sxs-lookup"><span data-stu-id="3801b-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3801b-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3801b-139">Examples</span></span>

<span data-ttu-id="3801b-140">O exemplo a seguir demonstra o uso das instruções de **SEparador** **MenuItem** e MenuItem:</span><span class="sxs-lookup"><span data-stu-id="3801b-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="3801b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3801b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3801b-142">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="3801b-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3801b-143">**POP-up**</span><span class="sxs-lookup"><span data-stu-id="3801b-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




