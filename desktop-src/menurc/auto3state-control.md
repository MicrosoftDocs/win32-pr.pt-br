---
title: Controle AUTO3STATE
description: Define uma caixa de seleção automática de três Estados.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menus de controle do AUTO3STATE e outros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084502"
---
# <a name="auto3state-control"></a><span data-ttu-id="f9ef9-104">Controle AUTO3STATE</span><span class="sxs-lookup"><span data-stu-id="f9ef9-104">AUTO3STATE control</span></span>

<span data-ttu-id="f9ef9-105">Define uma caixa de seleção automática de três Estados.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="f9ef9-106">O controle é uma caixa aberta com o texto fornecido posicionado à direita da caixa.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="f9ef9-107">Quando escolhido, a caixa avança automaticamente entre três Estados: marcada, desmarcada e desabilitada (cinza).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="f9ef9-108">O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="f9ef9-109"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="f9ef9-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="f9ef9-110">Estilos para o controle, que pode ser uma combinação do estilo **BS \_ AUTO3STATE** e dos seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="f9ef9-111">Se você não especificar um estilo, o estilo padrão será `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="f9ef9-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="f9ef9-112">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9ef9-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9ef9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ef9-114">**CAIXA de seleção automarca**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="f9ef9-115">Caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="f9ef9-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="f9ef9-116">**VERIFICAÇÃO**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="f9ef9-117">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="f9ef9-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="f9ef9-119">Estilos de janela</span><span class="sxs-lookup"><span data-stu-id="f9ef9-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 