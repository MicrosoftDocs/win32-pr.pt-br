---
title: Definindo nomes para o pré-processador
description: Você pode especificar a compilação condicional em um script, com base em se um nome é definido na linha de comando RC com a opção/d ou no arquivo ou em um arquivo de inclusão com a diretiva \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291882"
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

 

 




