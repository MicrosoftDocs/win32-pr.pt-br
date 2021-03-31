---
title: Controle EDITTEXT
description: Define um controle de edição que pertence à classe EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menus de controle do EDITTEXT e outros recursos
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640744"
---
# <a name="edittext-control"></a><span data-ttu-id="e519c-104">Controle EDITTEXT</span><span class="sxs-lookup"><span data-stu-id="e519c-104">EDITTEXT control</span></span>

<span data-ttu-id="e519c-105">Define um controle de edição que pertence à classe EDIT.</span><span class="sxs-lookup"><span data-stu-id="e519c-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="e519c-106">Ele cria uma região retangular na qual o usuário pode digitar e editar texto.</span><span class="sxs-lookup"><span data-stu-id="e519c-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="e519c-107">O controle exibe um cursor quando o usuário clica no mouse nele.</span><span class="sxs-lookup"><span data-stu-id="e519c-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="e519c-108">Em seguida, o usuário pode usar o teclado para inserir texto ou editar o texto existente.</span><span class="sxs-lookup"><span data-stu-id="e519c-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="e519c-109">As chaves de edição incluem as chaves Backspace e DELETE.</span><span class="sxs-lookup"><span data-stu-id="e519c-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="e519c-110">O usuário também pode usar o mouse para selecionar os caracteres a serem excluídos ou para selecionar o local para inserir novos caracteres.</span><span class="sxs-lookup"><span data-stu-id="e519c-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e519c-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="e519c-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e519c-112">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="e519c-112">Control styles.</span></span> <span data-ttu-id="e519c-113">Esse valor pode ser uma combinação dos estilos de classe de edição e dos seguintes estilos **: WS \_ TabStop**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** e **WS \_ Disabled**.</span><span class="sxs-lookup"><span data-stu-id="e519c-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="e519c-114">Se você não especificar um estilo, o estilo padrão será `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="e519c-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e519c-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e519c-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e519c-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e519c-116">Examples</span></span>

<span data-ttu-id="e519c-117">O exemplo a seguir demonstra o uso da instrução **EDITTEXT** :</span><span class="sxs-lookup"><span data-stu-id="e519c-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="e519c-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e519c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e519c-119">Editar controles</span><span class="sxs-lookup"><span data-stu-id="e519c-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 