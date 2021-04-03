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
# <a name="sample-resource-definition-file"></a>Arquivo de Resource-Definition de exemplo

O exemplo a seguir mostra um arquivo de script que define os recursos para um aplicativo denominado formas:

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

A instrução [**cursor**](cursor-resource.md) nomeia o recurso de cursor do aplicativo ShapesCursor e especifica as formas do arquivo de cursor. CUR, que contém a imagem para esse cursor.

A instrução [**Icon**](icon-resource.md) nomeia o recurso de ícone do aplicativo ShapesIcon e especifica as formas de arquivo de ícone. ICO, que contém a imagem para esse ícone.

A instrução de [**menu**](menu-resource.md) define um menu de aplicativo chamado **ShapesMenu**, um menu pop-up com cinco itens de menu.

O corpo da definição do menu, entre chaves, ou as palavras-chave **begin** e **end** , especifica cada item de menu e o identificador de menu que é retornado quando o usuário seleciona esse item. Por exemplo, o primeiro item no menu, **Clear**, retorna a ID de identificador de menu \_ Clear quando o usuário a seleciona. Os identificadores de menu são definidos no arquivo de cabeçalho do aplicativo, SHAPEs. H.

 

 




