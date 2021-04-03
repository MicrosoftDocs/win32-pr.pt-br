---
title: Arquivo de Resource-Definition de exemplo
description: Exemplo de arquivo de script que define os recursos para um aplicativo denominado formas.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005859"
---
# <a name="sample-resource-definition-file"></a><span data-ttu-id="5f12c-103">Arquivo de Resource-Definition de exemplo</span><span class="sxs-lookup"><span data-stu-id="5f12c-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="5f12c-104">O exemplo a seguir mostra um arquivo de script que define os recursos para um aplicativo denominado formas:</span><span class="sxs-lookup"><span data-stu-id="5f12c-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

<span data-ttu-id="5f12c-105">A instrução [**cursor**](cursor-resource.md) nomeia o recurso de cursor do aplicativo ShapesCursor e especifica as formas do arquivo de cursor. CUR, que contém a imagem para esse cursor.</span><span class="sxs-lookup"><span data-stu-id="5f12c-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="5f12c-106">A instrução [**Icon**](icon-resource.md) nomeia o recurso de ícone do aplicativo ShapesIcon e especifica as formas de arquivo de ícone. ICO, que contém a imagem para esse ícone.</span><span class="sxs-lookup"><span data-stu-id="5f12c-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="5f12c-107">A instrução de [**menu**](menu-resource.md) define um menu de aplicativo chamado **ShapesMenu**, um menu pop-up com cinco itens de menu.</span><span class="sxs-lookup"><span data-stu-id="5f12c-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="5f12c-108">O corpo da definição do menu, entre chaves, ou as palavras-chave **begin** e **end** , especifica cada item de menu e o identificador de menu que é retornado quando o usuário seleciona esse item.</span><span class="sxs-lookup"><span data-stu-id="5f12c-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="5f12c-109">Por exemplo, o primeiro item no menu, **Clear**, retorna a ID de identificador de menu \_ Clear quando o usuário a seleciona.</span><span class="sxs-lookup"><span data-stu-id="5f12c-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="5f12c-110">Os identificadores de menu são definidos no arquivo de cabeçalho do aplicativo, SHAPEs. H.</span><span class="sxs-lookup"><span data-stu-id="5f12c-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




