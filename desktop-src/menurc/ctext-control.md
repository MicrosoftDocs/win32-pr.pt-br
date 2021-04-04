---
title: Controle CTEXT
description: Define um controle de texto centralizado.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menus de controle do CTEXT e outros recursos
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084500"
---
# <a name="ctext-control"></a><span data-ttu-id="0b04d-104">Controle CTEXT</span><span class="sxs-lookup"><span data-stu-id="0b04d-104">CTEXT control</span></span>

<span data-ttu-id="0b04d-105">Define um controle de texto centralizado.</span><span class="sxs-lookup"><span data-stu-id="0b04d-105">Defines a centered-text control.</span></span> <span data-ttu-id="0b04d-106">O controle é um retângulo simples que exibe o texto fornecido centralizado no retângulo.</span><span class="sxs-lookup"><span data-stu-id="0b04d-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="0b04d-107">O texto é formatado antes de ser exibido.</span><span class="sxs-lookup"><span data-stu-id="0b04d-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="0b04d-108">As palavras que ultrapassaram o final de uma linha são automaticamente encapsuladas no início da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="0b04d-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="0b04d-109">Palavras que são maiores que a largura do controle são truncadas.</span><span class="sxs-lookup"><span data-stu-id="0b04d-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="0b04d-110">A instrução [**LTEXT**](ltext-control.md) , que pode ser usada somente em uma instrução Rep, define o texto, o identificador, as dimensões e os atributos do controle.</span><span class="sxs-lookup"><span data-stu-id="0b04d-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0b04d-111"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="0b04d-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="0b04d-112">Texto que deve ser centralizado na área retangular do controle.</span><span class="sxs-lookup"><span data-stu-id="0b04d-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0b04d-113"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="0b04d-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0b04d-114">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="0b04d-114">Control styles.</span></span> <span data-ttu-id="0b04d-115">Esse valor pode ser qualquer combinação dos seguintes estilos: **SS \_ Center**, **WS \_ TabStop** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0b04d-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0b04d-116">Se você não especificar um estilo, o estilo padrão será `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="0b04d-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="0b04d-117">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0b04d-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0b04d-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b04d-118">Examples</span></span>

<span data-ttu-id="0b04d-119">Este exemplo define um controle de texto centralizado que é rotulado como nome de arquivo:</span><span class="sxs-lookup"><span data-stu-id="0b04d-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="0b04d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b04d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b04d-121">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="0b04d-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0b04d-122">Editar controles</span><span class="sxs-lookup"><span data-stu-id="0b04d-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="0b04d-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="0b04d-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="0b04d-124">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="0b04d-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 