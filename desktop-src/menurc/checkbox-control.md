---
title: Controle de caixa de seleção (compilador de recurso)
description: Define um controle de caixa de seleção.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menus de controle de caixa de seleção e outros recursos
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105761270"
---
# <a name="checkbox-control"></a><span data-ttu-id="e46c9-104">Controle de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="e46c9-104">CHECKBOX control</span></span>

<span data-ttu-id="e46c9-105">Define um controle de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="e46c9-105">Defines a check box control.</span></span> <span data-ttu-id="e46c9-106">O controle é um pequeno retângulo (caixa de seleção) que tem o texto especificado exibido ao lado (normalmente, à direita).</span><span class="sxs-lookup"><span data-stu-id="e46c9-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="e46c9-107">Quando o usuário seleciona o controle, o controle realça o retângulo e envia uma mensagem para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="e46c9-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="e46c9-108">A instrução **CheckBox** , que só pode ser usada em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos do controle.</span><span class="sxs-lookup"><span data-stu-id="e46c9-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e46c9-109"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="e46c9-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="e46c9-110">Texto a ser exibido à direita do controle.</span><span class="sxs-lookup"><span data-stu-id="e46c9-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e46c9-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="e46c9-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e46c9-112">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="e46c9-112">Control styles.</span></span> <span data-ttu-id="e46c9-113">Esse valor pode ser uma combinação da **\_ caixa de seleção BS** do estilo de classe de botão e dos estilos de **\_ grupo** **WS \_ TabStop** e WS.</span><span class="sxs-lookup"><span data-stu-id="e46c9-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="e46c9-114">Se você não especificar um estilo, o estilo padrão será `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="e46c9-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e46c9-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e46c9-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e46c9-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e46c9-116">Examples</span></span>

<span data-ttu-id="e46c9-117">Este exemplo define um controle de caixa de seleção que é rotulado como itálico:</span><span class="sxs-lookup"><span data-stu-id="e46c9-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="e46c9-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e46c9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e46c9-119">**CAIXA de seleção automarca**</span><span class="sxs-lookup"><span data-stu-id="e46c9-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="e46c9-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="e46c9-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="e46c9-121">Caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="e46c9-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="e46c9-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="e46c9-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="e46c9-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="e46c9-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 