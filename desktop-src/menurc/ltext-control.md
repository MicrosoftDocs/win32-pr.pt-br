---
title: Controle LTEXT
description: Define um controle de texto alinhado à esquerda.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menus de controle do LTEXT e outros recursos
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105755911"
---
# <a name="ltext-control"></a><span data-ttu-id="a1783-104">Controle LTEXT</span><span class="sxs-lookup"><span data-stu-id="a1783-104">LTEXT control</span></span>

<span data-ttu-id="a1783-105">Define um controle de texto alinhado à esquerda.</span><span class="sxs-lookup"><span data-stu-id="a1783-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="a1783-106">O controle é um retângulo simples que exibe o texto determinado alinhado à esquerda no retângulo.</span><span class="sxs-lookup"><span data-stu-id="a1783-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="a1783-107">O texto é formatado antes de ser exibido.</span><span class="sxs-lookup"><span data-stu-id="a1783-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="a1783-108">As palavras que ultrapassaram o final de uma linha são automaticamente encapsuladas no início da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="a1783-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="a1783-109">Palavras que são maiores que a largura do controle são truncadas.</span><span class="sxs-lookup"><span data-stu-id="a1783-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="a1783-110">A instrução **LTEXT** , que pode ser usada somente em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos do controle.</span><span class="sxs-lookup"><span data-stu-id="a1783-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a1783-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="a1783-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a1783-112">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="a1783-112">Control styles.</span></span> <span data-ttu-id="a1783-113">Esse valor pode ser qualquer combinação do estilo **de \_ botão de opção BS** e dos seguintes estilos: **SS \_ Left**, **WS \_ TabStop** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="a1783-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="a1783-114">Se você não especificar um estilo, o estilo padrão será `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="a1783-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="a1783-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a1783-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a1783-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1783-116">Examples</span></span>

<span data-ttu-id="a1783-117">Este exemplo define um controle de texto alinhado à esquerda que é rotulado como nome de arquivo:</span><span class="sxs-lookup"><span data-stu-id="a1783-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="a1783-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1783-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1783-119">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="a1783-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="a1783-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="a1783-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="a1783-121">Editar controles</span><span class="sxs-lookup"><span data-stu-id="a1783-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="a1783-122">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="a1783-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 