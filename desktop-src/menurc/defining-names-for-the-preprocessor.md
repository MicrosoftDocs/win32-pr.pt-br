---
title: Definindo nomes para o pré-processador
description: Você pode especificar a compilação condicional em um script, com base em se um nome é definido na linha de comando RC com a opção/d ou no arquivo ou em um arquivo de inclusão com a diretiva \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3bcf9c02b5a4da4487b0c82de8d8b0223662cb30f9529e82204fc66a3de91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972105"
---
# <a name="defining-names-for-the-preprocessor"></a>Definindo nomes para o pré-processador

Você pode especificar a compilação condicional em um script, com base no fato de um nome ser definido na linha de comando RC com a opção **/d** ou no arquivo ou em um arquivo de inclusão com a diretiva [**\# definir**](-define.md) .

Por exemplo, suponha que seu aplicativo tenha um menu pop-up que deve aparecer apenas com versões de depuração do aplicativo. Quando você compila o aplicativo para uso normal, o menu não é incluído. O exemplo a seguir mostra as instruções que podem ser adicionadas ao arquivo de definição de recurso para definir um menu de depuração:

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

Ao compilar recursos para uma versão de depuração do aplicativo, você pode incluir o menu Depurar usando o seguinte comando:

**RC-d depurar MyApp. rc**

Para compilar recursos para uma versão normal do aplicativo? um que não inclui o menu Depurar? você pode usar o seguinte comando:

**RC MyApp. rc**

 

 




