---
title: Controle LISTBOX (menus e outros recursos)
description: Define controles comumente usados para uma caixa de diálogo ou janela. O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de filename) da qual o usuário pode selecionar.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menus de controle de caixa de listagem e outros recursos
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084527"
---
# <a name="listbox-control"></a><span data-ttu-id="19e77-105">Controle LISTBOX</span><span class="sxs-lookup"><span data-stu-id="19e77-105">LISTBOX control</span></span>

<span data-ttu-id="19e77-106">Define controles comumente usados para uma caixa de diálogo ou janela.</span><span class="sxs-lookup"><span data-stu-id="19e77-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="19e77-107">O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de filename) da qual o usuário pode selecionar.</span><span class="sxs-lookup"><span data-stu-id="19e77-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="19e77-108">A instrução **ListBox** , que só pode ser usada em uma [**DIALOGEX**](dialogex-resource.md) ou instrução de **janela** , define o identificador, as dimensões e os atributos de uma janela de controle.</span><span class="sxs-lookup"><span data-stu-id="19e77-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="19e77-109"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="19e77-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="19e77-110">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="19e77-110">Control styles.</span></span> <span data-ttu-id="19e77-111">Esse valor pode ser uma combinação dos estilos de classe da caixa de listagem e de qualquer um dos seguintes estilos: **WS \_ Border** e **WS \_ VSCROLL**.</span><span class="sxs-lookup"><span data-stu-id="19e77-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="19e77-112">Se você não especificar um estilo, o estilo padrão será `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="19e77-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="19e77-113">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="19e77-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="19e77-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19e77-114">Examples</span></span>

<span data-ttu-id="19e77-115">Este exemplo define um controle de caixa de listagem cujo identificador é 101:</span><span class="sxs-lookup"><span data-stu-id="19e77-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="19e77-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="19e77-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e77-117">**COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="19e77-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="19e77-118">Caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="19e77-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 