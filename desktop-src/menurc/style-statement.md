---
title: Instrução de estilo
description: Define o estilo de janela da caixa de diálogo. O estilo da janela especifica se a caixa é uma janela pop-up ou filho.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menus de instrução de estilo e outros recursos
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365953"
---
# <a name="style-statement"></a><span data-ttu-id="8e63e-105">Instrução de estilo</span><span class="sxs-lookup"><span data-stu-id="8e63e-105">STYLE statement</span></span>

<span data-ttu-id="8e63e-106">Define o estilo de janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e63e-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="8e63e-107">O estilo da janela especifica se a caixa é uma janela pop-up ou filho.</span><span class="sxs-lookup"><span data-stu-id="8e63e-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="8e63e-108"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="8e63e-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="8e63e-109">O estilo da janela.</span><span class="sxs-lookup"><span data-stu-id="8e63e-109">The window style.</span></span> <span data-ttu-id="8e63e-110">Esse parâmetro pode ser um valor inteiro ou uma combinação de valores de estilo de janela (como **WS \_ Caption** e **WS \_ SYSMENU**) e valores de estilo de caixa de diálogo (como o **DS \_ Center**).</span><span class="sxs-lookup"><span data-stu-id="8e63e-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="8e63e-111">Para obter uma lista de estilos de janela, consulte [estilos de janela](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="8e63e-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="8e63e-112">Para obter uma lista de estilos de caixa de diálogo, consulte [estilos de modelo de caixa de diálogo](../dlgbox/about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="8e63e-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="8e63e-113">Se você usar os valores de estilo da janela ou da caixa de diálogo, deverá incluir Windows. h.</span><span class="sxs-lookup"><span data-stu-id="8e63e-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 