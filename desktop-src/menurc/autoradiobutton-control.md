---
title: Controle AUTORADIOBUTTON
description: Define um controle de botão de opção automático. Esse controle executa automaticamente a exclusão mútua com os outros controles AUTORADIOBUTTON no mesmo grupo. Quando o botão é escolhido, o aplicativo é notificado com bilhão \_ clicado.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menus de controle de AUTORADIOBUTTON e outros recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638519"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="6b03a-106">Controle AUTORADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="6b03a-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="6b03a-107">Define um controle de botão de opção automático.</span><span class="sxs-lookup"><span data-stu-id="6b03a-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="6b03a-108">Esse controle executa automaticamente a exclusão mútua com os outros controles **AUTORADIOBUTTON** no mesmo grupo.</span><span class="sxs-lookup"><span data-stu-id="6b03a-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="6b03a-109">Quando o botão é escolhido, o aplicativo é notificado com **bilhão \_ clicado**.</span><span class="sxs-lookup"><span data-stu-id="6b03a-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="6b03a-110"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="6b03a-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="6b03a-111">Texto que será exibido ao lado do botão de opção.</span><span class="sxs-lookup"><span data-stu-id="6b03a-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="6b03a-112"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="6b03a-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="6b03a-113">Estilos para o botão de opção automático, que pode ser uma combinação de estilos de classe de botão e os seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="6b03a-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="6b03a-114">Se você não especificar um estilo, o estilo padrão será `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="6b03a-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="6b03a-115">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6b03a-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b03a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b03a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b03a-117">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="6b03a-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="6b03a-118">Botões de opção</span><span class="sxs-lookup"><span data-stu-id="6b03a-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="6b03a-119">**ÍNDICES**</span><span class="sxs-lookup"><span data-stu-id="6b03a-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




