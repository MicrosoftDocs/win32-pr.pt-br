---
title: Controle GROUPBOX (menus e outros recursos)
description: Define um controle de caixa de grupo. O controle é um retângulo que agrupa outros controles juntos. Os controles são agrupados desenhando uma borda em torno deles e exibindo o texto fornecido no canto superior esquerdo.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menus de controle de GROUPBOX e outros recursos
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104006857"
---
# <a name="groupbox-control"></a><span data-ttu-id="cff22-106">Controle GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="cff22-106">GROUPBOX control</span></span>

<span data-ttu-id="cff22-107">Define um controle de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="cff22-107">Defines a group box control.</span></span> <span data-ttu-id="cff22-108">O controle é um retângulo que agrupa outros controles juntos.</span><span class="sxs-lookup"><span data-stu-id="cff22-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="cff22-109">Os controles são agrupados desenhando uma borda em torno deles e exibindo o texto fornecido no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="cff22-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="cff22-110">A instrução **GroupBox** , que pode ser usada somente em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos de uma janela de controle.</span><span class="sxs-lookup"><span data-stu-id="cff22-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="cff22-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="cff22-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="cff22-112">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="cff22-112">Control styles.</span></span> <span data-ttu-id="cff22-113">Esse valor pode ser uma combinação do botão classe estilo **BS \_ GroupBox** e os estilos **WS \_ TabStop** e **WS \_ Disabled** .</span><span class="sxs-lookup"><span data-stu-id="cff22-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="cff22-114">Se você não especificar um estilo, o estilo padrão será **BS \_ GroupBox**.</span><span class="sxs-lookup"><span data-stu-id="cff22-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="cff22-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cff22-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cff22-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cff22-116">Remarks</span></span>

<span data-ttu-id="cff22-117">Quando o estilo contém **WS \_ TabStop** ou o texto especifica um acelerador, a Tabulação ou o pressionamento da tecla acelerador move o foco para o primeiro controle dentro do grupo.</span><span class="sxs-lookup"><span data-stu-id="cff22-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="cff22-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cff22-118">Examples</span></span>

<span data-ttu-id="cff22-119">Este exemplo define um controle de caixa de grupo que é rotulado como opções:</span><span class="sxs-lookup"><span data-stu-id="cff22-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="cff22-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cff22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff22-121">Caixas de grupo</span><span class="sxs-lookup"><span data-stu-id="cff22-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




