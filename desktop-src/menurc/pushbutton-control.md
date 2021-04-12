---
title: Controle de pressão (menus e outros recursos)
description: Define um controle de botão de ação. O controle é um retângulo com cantos arredondados contendo o texto fornecido. O texto é centralizado no controle. O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menus de controle de pressão e outros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294058"
---
# <a name="pushbutton-control"></a><span data-ttu-id="ed1b4-107">Controle de supressão</span><span class="sxs-lookup"><span data-stu-id="ed1b4-107">PUSHBUTTON control</span></span>

<span data-ttu-id="ed1b4-108">Define um controle de botão de ação.</span><span class="sxs-lookup"><span data-stu-id="ed1b4-108">Defines a push-button control.</span></span> <span data-ttu-id="ed1b4-109">O controle é um retângulo com cantos arredondados contendo o texto fornecido.</span><span class="sxs-lookup"><span data-stu-id="ed1b4-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="ed1b4-110">O texto é centralizado no controle.</span><span class="sxs-lookup"><span data-stu-id="ed1b4-110">The text is centered in the control.</span></span> <span data-ttu-id="ed1b4-111">O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.</span><span class="sxs-lookup"><span data-stu-id="ed1b4-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="ed1b4-112"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="ed1b4-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="ed1b4-113">Estilos para o botão de pressão, que pode ser uma combinação do estilo de **\_ pressão de BS** e dos seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="ed1b4-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="ed1b4-114">Se você não especificar um estilo, o estilo padrão será `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="ed1b4-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="ed1b4-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ed1b4-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed1b4-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed1b4-116">Examples</span></span>

<span data-ttu-id="ed1b4-117">O exemplo a seguir demonstra o uso da instrução de **pressão** :</span><span class="sxs-lookup"><span data-stu-id="ed1b4-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="ed1b4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed1b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1b4-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="ed1b4-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="ed1b4-120">Botões de push</span><span class="sxs-lookup"><span data-stu-id="ed1b4-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 