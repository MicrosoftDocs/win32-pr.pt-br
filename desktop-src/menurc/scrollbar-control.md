---
title: Controle SCROLLBAR
description: Define um controle de barra de rolagem.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menus de controle de barra de ROLAgem e outros recursos
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084541"
---
# <a name="scrollbar-control"></a><span data-ttu-id="c1c56-104">Controle SCROLLBAR</span><span class="sxs-lookup"><span data-stu-id="c1c56-104">SCROLLBAR control</span></span>

<span data-ttu-id="c1c56-105">Define um controle de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="c1c56-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="c1c56-106">O controle é um retângulo que contém uma caixa de rolagem e tem setas de direção em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="c1c56-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="c1c56-107">O controle de barra de rolagem envia uma mensagem de notificação para seu pai sempre que o usuário clica no controle.</span><span class="sxs-lookup"><span data-stu-id="c1c56-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="c1c56-108">O pai é responsável por atualizar a posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="c1c56-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="c1c56-109">Os controles de barra de rolagem podem ser posicionados em qualquer lugar em uma janela e usados sempre que necessário para fornecer a entrada de rolagem.</span><span class="sxs-lookup"><span data-stu-id="c1c56-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="c1c56-110"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="c1c56-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="c1c56-111">Zero ou uma combinação dos seguintes estilos: **WS \_ TabStop**, **WS \_ Group** e **WS \_ desabilitados**.</span><span class="sxs-lookup"><span data-stu-id="c1c56-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="c1c56-112">Além desses estilos, o parâmetro *Style* pode conter uma combinação (ou nenhum) dos estilos de classe ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="c1c56-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="c1c56-113">Se você não especificar um estilo, o estilo padrão será **SBS \_ na horizontal**.</span><span class="sxs-lookup"><span data-stu-id="c1c56-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="c1c56-114">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c1c56-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="c1c56-115">Observe que você não pode especificar o texto para este controle.</span><span class="sxs-lookup"><span data-stu-id="c1c56-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="c1c56-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1c56-116">Examples</span></span>

<span data-ttu-id="c1c56-117">O exemplo a seguir demonstra o uso da instrução **ScrollBar** :</span><span class="sxs-lookup"><span data-stu-id="c1c56-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="c1c56-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c56-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c56-119">Barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="c1c56-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 