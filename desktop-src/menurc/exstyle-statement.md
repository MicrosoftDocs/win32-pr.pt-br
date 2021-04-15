---
title: Instrução filestyle
description: Define os estilos de janela estendidos para uma caixa de diálogo. Em uma definição de recurso, a instrução filestyle é colocada com as instruções opcionais antes do início do corpo da definição de recurso.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menus de instruções do filestyle e outros recursos
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454014"
---
# <a name="exstyle-statement"></a><span data-ttu-id="b2cc5-105">Instrução filestyle</span><span class="sxs-lookup"><span data-stu-id="b2cc5-105">EXSTYLE statement</span></span>

<span data-ttu-id="b2cc5-106">Define os estilos de janela estendidos para uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b2cc5-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="b2cc5-107">Em uma definição de recurso, a instrução **filestyle** é colocada com as instruções opcionais antes do início do corpo da definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="b2cc5-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="b2cc5-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo estendido*</span><span class="sxs-lookup"><span data-stu-id="b2cc5-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="b2cc5-109">Estilo de janela estendida para a caixa de diálogo ou controle.</span><span class="sxs-lookup"><span data-stu-id="b2cc5-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="b2cc5-110">Para obter uma lista de estilos de janela estendidos, consulte [**estilos de janela estendidos**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="b2cc5-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2cc5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2cc5-111">Remarks</span></span>

<span data-ttu-id="b2cc5-112">Para controles, os estilos estendidos são especificados após a opção de *estilo* na instrução Control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="b2cc5-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="b2cc5-113">Para obter mais informações, consulte a instrução de definição de recurso para o controle individual.</span><span class="sxs-lookup"><span data-stu-id="b2cc5-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2cc5-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2cc5-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cc5-115">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-116">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-117">**'**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-118">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-119">**POP-up**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-121">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b2cc5-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b2cc5-122">Recurso definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="b2cc5-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 