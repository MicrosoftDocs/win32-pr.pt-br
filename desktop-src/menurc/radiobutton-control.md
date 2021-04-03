---
title: Controle RADIOBUTTON
description: Define um controle de botão de opção.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menus de controle RADIOBUTTON e outros recursos
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007547"
---
# <a name="radiobutton-control"></a><span data-ttu-id="5abc4-104">Controle RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="5abc4-104">RADIOBUTTON control</span></span>

<span data-ttu-id="5abc4-105">Define um controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="5abc4-105">Defines a radio-button control.</span></span> <span data-ttu-id="5abc4-106">O controle é um círculo pequeno que tem o texto fornecido ao lado dele, normalmente à direita.</span><span class="sxs-lookup"><span data-stu-id="5abc4-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="5abc4-107">O controle realça o círculo e envia uma mensagem para sua janela pai quando o usuário seleciona o botão.</span><span class="sxs-lookup"><span data-stu-id="5abc4-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="5abc4-108">O controle remove o realce e envia uma mensagem quando o botão é selecionado na próxima vez.</span><span class="sxs-lookup"><span data-stu-id="5abc4-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="5abc4-109"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="5abc4-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="5abc4-110">Estilos para o botão de opção, que pode ser uma combinação de estilos de classe de botão e os seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="5abc4-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="5abc4-111">Se você não especificar um estilo, o estilo padrão será `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="5abc4-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="5abc4-112">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5abc4-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5abc4-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5abc4-113">Examples</span></span>

<span data-ttu-id="5abc4-114">O exemplo a seguir demonstra o uso da instrução **RadioButton** :</span><span class="sxs-lookup"><span data-stu-id="5abc4-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="5abc4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5abc4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abc4-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="5abc4-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="5abc4-117">Botões de opção</span><span class="sxs-lookup"><span data-stu-id="5abc4-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 