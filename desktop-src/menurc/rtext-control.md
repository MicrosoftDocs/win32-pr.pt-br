---
title: Controle RTEXT
description: Define um controle de texto alinhado à direita.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menus de controle do RTEXT e outros recursos
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454059"
---
# <a name="rtext-control"></a><span data-ttu-id="75bf3-104">Controle RTEXT</span><span class="sxs-lookup"><span data-stu-id="75bf3-104">RTEXT control</span></span>

<span data-ttu-id="75bf3-105">Define um controle de texto alinhado à direita.</span><span class="sxs-lookup"><span data-stu-id="75bf3-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="75bf3-106">O controle é um retângulo simples que exibe o texto determinado alinhado à direita no retângulo.</span><span class="sxs-lookup"><span data-stu-id="75bf3-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="75bf3-107">O texto é formatado antes de ser exibido.</span><span class="sxs-lookup"><span data-stu-id="75bf3-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="75bf3-108">As palavras que ultrapassaram o final de uma linha são automaticamente encapsuladas no início da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="75bf3-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="75bf3-109">Palavras que são maiores que a largura do controle são truncadas.</span><span class="sxs-lookup"><span data-stu-id="75bf3-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="75bf3-110">A instrução **RTEXT** , que pode ser usada somente em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos do controle.</span><span class="sxs-lookup"><span data-stu-id="75bf3-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="75bf3-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="75bf3-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="75bf3-112">Estilos para o controle de texto, que pode ser qualquer combinação dos seguintes: **WS \_ TabStop** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="75bf3-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="75bf3-113">Se você não especificar um estilo, o estilo padrão será `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="75bf3-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="75bf3-114">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="75bf3-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="75bf3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75bf3-115">Examples</span></span>

<span data-ttu-id="75bf3-116">O exemplo a seguir demonstra o uso da instrução **RTEXT** :</span><span class="sxs-lookup"><span data-stu-id="75bf3-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="75bf3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="75bf3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bf3-118">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="75bf3-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="75bf3-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="75bf3-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="75bf3-120">Editar controles</span><span class="sxs-lookup"><span data-stu-id="75bf3-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="75bf3-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="75bf3-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 