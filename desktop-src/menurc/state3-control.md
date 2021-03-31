---
title: Controle STATE3
description: Define um controle de caixa de seleção de três Estados. O controle é idêntico a uma caixa de seleção, exceto que ele tem três Estados marcados, desmarcados e desabilitados (acinzentados).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menus de controle do STATE3 e outros recursos
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638445"
---
# <a name="state3-control"></a><span data-ttu-id="0d5ff-105">Controle STATE3</span><span class="sxs-lookup"><span data-stu-id="0d5ff-105">STATE3 control</span></span>

<span data-ttu-id="0d5ff-106">Define um controle de caixa de seleção de três Estados.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-106">Defines a three-state check box control.</span></span> <span data-ttu-id="0d5ff-107">O controle é idêntico a uma [**caixa de seleção**](checkbox-control.md), exceto pelo fato de que ele tem três Estados: marcada, desmarcada e desabilitada (cinza).</span><span class="sxs-lookup"><span data-stu-id="0d5ff-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0d5ff-108"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="0d5ff-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="0d5ff-109">Texto a ser exibido à direita do controle.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0d5ff-110"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="0d5ff-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0d5ff-111">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-111">Control styles.</span></span> <span data-ttu-id="0d5ff-112">Esse valor pode ser uma combinação do botão classe estilo **BS \_ 3STATE** e os estilos **WS \_ TabStop** e **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="0d5ff-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="0d5ff-113">Se você não especificar um estilo, o estilo padrão será `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0d5ff-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0d5ff-114">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d5ff-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0d5ff-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d5ff-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5ff-116">**CAIXA de seleção automarca**</span><span class="sxs-lookup"><span data-stu-id="0d5ff-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="0d5ff-117">Caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="0d5ff-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="0d5ff-118">**VERIFICAÇÃO**</span><span class="sxs-lookup"><span data-stu-id="0d5ff-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="0d5ff-119">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="0d5ff-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




