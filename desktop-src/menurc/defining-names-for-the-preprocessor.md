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
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="70835-103">Definindo nomes para o pré-processador</span><span class="sxs-lookup"><span data-stu-id="70835-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="70835-104">Você pode especificar a compilação condicional em um script, com base no fato de um nome ser definido na linha de comando RC com a opção **/d** ou no arquivo ou em um arquivo de inclusão com a diretiva [**\# definir**](-define.md) .</span><span class="sxs-lookup"><span data-stu-id="70835-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="70835-105">Por exemplo, suponha que seu aplicativo tenha um menu pop-up que deve aparecer apenas com versões de depuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70835-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="70835-106">Quando você compila o aplicativo para uso normal, o menu não é incluído.</span><span class="sxs-lookup"><span data-stu-id="70835-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="70835-107">O exemplo a seguir mostra as instruções que podem ser adicionadas ao arquivo de definição de recurso para definir um menu de depuração:</span><span class="sxs-lookup"><span data-stu-id="70835-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

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

<span data-ttu-id="70835-108">Ao compilar recursos para uma versão de depuração do aplicativo, você pode incluir o menu Depurar usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="70835-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="70835-109">**RC-d depurar MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="70835-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="70835-110">Para compilar recursos para uma versão normal do aplicativo? um que não inclui o menu Depurar? você pode usar o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="70835-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="70835-111">**RC MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="70835-111">**rc myapp.rc**</span></span>

 

 




