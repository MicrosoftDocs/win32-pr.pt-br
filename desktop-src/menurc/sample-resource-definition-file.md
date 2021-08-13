---
title: Arquivo Resource-Definition exemplo
description: Arquivo de script de exemplo que define os recursos para um aplicativo chamado Formas.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141258148b4e7a21d625a44b7f03d5e383c318d10447e050891f32b397c4283d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119225996"
---
# <a name="sample-resource-definition-file"></a>Arquivo Resource-Definition exemplo

O exemplo a seguir mostra um arquivo de script que define os recursos para um aplicativo chamado Formas:

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

A [**instrução CURSOR**](cursor-resource.md) nomeia o recurso de cursor do aplicativo ShapesCursor e especifica o arquivo de cursor SHAPES. CUR, que contém a imagem desse cursor.

A [**instrução ICON**](icon-resource.md) nomeia o recurso de ícone do aplicativo ShapesIcon e especifica o arquivo de ícone SHAPES. ICO, que contém a imagem para esse ícone.

A [**instrução MENU**](menu-resource.md) define um menu de aplicativo chamado **ShapesMenu**, um menu pop-up com cinco itens de menu.

O corpo da definição de menu, entre as chaves ou as palavras-chave **BEGIN** e **END,** especifica cada item de menu e o identificador de menu que é retornado quando o usuário seleciona esse item. Por exemplo, o primeiro item no menu, **Limpar**, retorna a ID do identificador de menu \_ CLEAR quando o usuário a seleciona. Os identificadores de menu são definidos no arquivo de header do aplicativo SHAPES.H.

 

 




