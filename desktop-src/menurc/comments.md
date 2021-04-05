---
title: Comentários (menus e outros recursos)
description: O RC dá suporte à sintaxe em estilo C para comentários de linha única e para bloquear comentários. Os comentários de linha única começam com duas barras (//) e são executados até o final da linha. Veja a seguir um exemplo de uma instrução de recurso seguida por um comentário de linha única.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644181"
---
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="c1e89-105">Comentários (menus e outros recursos)</span><span class="sxs-lookup"><span data-stu-id="c1e89-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="c1e89-106">O RC dá suporte à sintaxe em estilo C para comentários de linha única e para bloquear comentários.</span><span class="sxs-lookup"><span data-stu-id="c1e89-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="c1e89-107">Os comentários de linha única começam com duas barras (//) e são executados até o final da linha.</span><span class="sxs-lookup"><span data-stu-id="c1e89-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="c1e89-108">Veja a seguir um exemplo de uma instrução de recurso seguida por um comentário de linha única.</span><span class="sxs-lookup"><span data-stu-id="c1e89-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="c1e89-109">Os comentários de bloco começam com um delimitador de abertura (/ \* ) e são executados para um delimitador de fechamento ( \* /).</span><span class="sxs-lookup"><span data-stu-id="c1e89-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="c1e89-110">Os comentários não podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="c1e89-110">Comments do not nest.</span></span> <span data-ttu-id="c1e89-111">Veja a seguir um exemplo de um comentário de bloco no início de um arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="c1e89-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




