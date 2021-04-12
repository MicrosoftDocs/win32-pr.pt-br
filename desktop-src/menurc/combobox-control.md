---
title: Controle COMBOBOX (menus e outros recursos)
description: Define um controle de caixa de combinação (uma caixa de combinação).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menus de controle de COMBOBOX e outros recursos
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365906"
---
# <a name="combobox-control"></a><span data-ttu-id="475f4-104">Controle COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="475f4-104">COMBOBOX control</span></span>

<span data-ttu-id="475f4-105">Define um controle de caixa de combinação (uma caixa de combinação).</span><span class="sxs-lookup"><span data-stu-id="475f4-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="475f4-106">Uma caixa de combinação consiste em uma caixa de texto estática ou em uma caixa de edição combinada com uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="475f4-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="475f4-107">A caixa de listagem pode ser exibida em todos os momentos ou obtida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="475f4-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="475f4-108">Se a caixa de combinação contiver uma caixa de texto estática, a caixa de texto sempre exibirá a seleção (se houver) na parte da caixa de listagem da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="475f4-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="475f4-109">Se ele usar uma caixa de edição, o usuário poderá digitar a seleção desejada; a caixa de listagem realça o primeiro item (se houver) que corresponde ao que o usuário inseriu na caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="475f4-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="475f4-110">O usuário pode selecionar o item realçado na caixa de listagem para concluir a escolha.</span><span class="sxs-lookup"><span data-stu-id="475f4-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="475f4-111">Além disso, a caixa de combinação pode ser desenhada pelo proprietário e da altura fixa ou variável.</span><span class="sxs-lookup"><span data-stu-id="475f4-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="475f4-112"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="475f4-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="475f4-113">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="475f4-113">Control styles.</span></span> <span data-ttu-id="475f4-114">Esse valor pode ser uma combinação dos estilos de classe COMBOBOX e de qualquer um dos seguintes estilos **: \_ WS TabStop**, **WS \_ Group**, **WS \_ VSCROLL** e **WS \_ Disabled**.</span><span class="sxs-lookup"><span data-stu-id="475f4-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="475f4-115">Se você não especificar um estilo, o estilo padrão será `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="475f4-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="475f4-116">O parâmetro *Height* aplica-se à altura de uma caixa de combinação com uma lista suspensa totalmente expandida.</span><span class="sxs-lookup"><span data-stu-id="475f4-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="475f4-117">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="475f4-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="475f4-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="475f4-118">Examples</span></span>

<span data-ttu-id="475f4-119">Este exemplo define um controle de caixa de combinação com uma barra de rolagem vertical:</span><span class="sxs-lookup"><span data-stu-id="475f4-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="475f4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="475f4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475f4-121">Caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="475f4-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 