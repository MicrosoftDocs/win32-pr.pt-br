---
title: Controle de caixa de seleção
description: Define um controle de caixa de seleção automática.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menus de controle de caixa de seleção AUTOe outros recursos
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640664"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="3a51b-104">Controle de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="3a51b-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="3a51b-105">Define um controle de caixa de seleção automática.</span><span class="sxs-lookup"><span data-stu-id="3a51b-105">Defines an automatic check box control.</span></span> <span data-ttu-id="3a51b-106">O controle é um pequeno retângulo (caixa de seleção) que tem o texto especificado exibido ao lado (normalmente, à direita).</span><span class="sxs-lookup"><span data-stu-id="3a51b-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="3a51b-107">Quando o usuário escolhe o controle, o controle realça o retângulo e envia uma mensagem para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="3a51b-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="3a51b-108">A instrução **AUTOCHECKBOX** só pode ser usada no corpo de uma instrução [**Dialog**](dialog-resource.md) ou [**DIALOGEX**](dialogex-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="3a51b-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="3a51b-109"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="3a51b-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="3a51b-110">Estilos do controle.</span><span class="sxs-lookup"><span data-stu-id="3a51b-110">Styles of the control.</span></span> <span data-ttu-id="3a51b-111">Esse valor pode ser uma combinação dos estilos de classe de botão **BS \_ AUTOCHECKBOX** e **WS \_ TabStop** e **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="3a51b-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="3a51b-112">Se você não especificar um estilo, o estilo padrão será `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="3a51b-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="3a51b-113">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3a51b-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a51b-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a51b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a51b-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="3a51b-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="3a51b-116">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="3a51b-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="3a51b-117">**VERIFICAÇÃO**</span><span class="sxs-lookup"><span data-stu-id="3a51b-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="3a51b-118">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="3a51b-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="3a51b-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="3a51b-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 