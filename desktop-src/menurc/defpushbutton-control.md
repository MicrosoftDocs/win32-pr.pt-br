---
title: Controle DEFPUSHBUTTON
description: Define um controle de botão de push padrão.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menus de controle do DEFPUSHBUTTON e outros recursos
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105768681"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="d0369-104">Controle DEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="d0369-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="d0369-105">Define um controle de botão de push padrão.</span><span class="sxs-lookup"><span data-stu-id="d0369-105">Defines a default push-button control.</span></span> <span data-ttu-id="d0369-106">O controle é um pequeno retângulo com um contorno em negrito que representa a resposta padrão para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d0369-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="d0369-107">O texto fornecido é exibido dentro do botão.</span><span class="sxs-lookup"><span data-stu-id="d0369-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="d0369-108">O controle realça o botão da maneira usual quando o usuário clica no mouse e envia uma mensagem para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="d0369-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="d0369-109"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="d0369-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="d0369-110">Texto que deve ser centralizado na área retangular do controle.</span><span class="sxs-lookup"><span data-stu-id="d0369-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d0369-111"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="d0369-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d0369-112">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="d0369-112">Control styles.</span></span> <span data-ttu-id="d0369-113">Esse valor pode ser uma combinação dos seguintes estilos: **BS \_ DEFPUSHBUTTON**, **WS \_ TabStop**, **WS \_ Group** e **WS \_ Disabled**.</span><span class="sxs-lookup"><span data-stu-id="d0369-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="d0369-114">Se você não especificar um estilo, o estilo padrão será `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="d0369-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="d0369-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d0369-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0369-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0369-116">Examples</span></span>

<span data-ttu-id="d0369-117">Este exemplo define um controle de botão de push padrão que é rotulado como cancelar:</span><span class="sxs-lookup"><span data-stu-id="d0369-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="d0369-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0369-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0369-119">Botões de push</span><span class="sxs-lookup"><span data-stu-id="d0369-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="d0369-120">**BOTÃO**</span><span class="sxs-lookup"><span data-stu-id="d0369-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="d0369-121">**ÍNDICES**</span><span class="sxs-lookup"><span data-stu-id="d0369-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




