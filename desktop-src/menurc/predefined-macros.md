---
title: Macros predefinidas
description: O RC não oferece suporte às macros predefinidas ANSI C ( \_ \_ Date \_ \_ , \_ \_ File \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ). Portanto, você não pode incluir essas macros em arquivos de cabeçalho que serão incluídas no script de recurso.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084064"
---
# <a name="predefined-macros"></a><span data-ttu-id="d9357-104">Macros predefinidas</span><span class="sxs-lookup"><span data-stu-id="d9357-104">Predefined Macros</span></span>

<span data-ttu-id="d9357-105">O RC não oferece suporte às macros predefinidas ANSI C (**\_ \_ Date \_ \_**, **\_ \_ File \_ \_**, **\_ \_ line \_ \_**, **\_ \_ stdc \_ \_**, **\_ \_ time \_ \_**, **\_ \_ timestamp \_ ). \_**</span><span class="sxs-lookup"><span data-stu-id="d9357-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="d9357-106">Portanto, você não pode incluir essas macros em arquivos de cabeçalho que serão incluídas no script de recurso.</span><span class="sxs-lookup"><span data-stu-id="d9357-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="d9357-107">O RC define \_ o RC chamado, que permite que você compile de forma condicional partes dos arquivos de cabeçalho, dependendo se o compilador é o compilador C ou o compilador RC.</span><span class="sxs-lookup"><span data-stu-id="d9357-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="d9357-108">Isso é importante porque o compilador RC dá suporte apenas a um subconjunto das instruções que um compilador C dará suporte.</span><span class="sxs-lookup"><span data-stu-id="d9357-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="d9357-109">Para compilar condicionalmente seu código com o compilador RC, envolva o código que o RC não pode compilar com \# ifndef RC \_ invocado e **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="d9357-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="d9357-110">O exemplo a seguir é extraído das amostras do SDK.</span><span class="sxs-lookup"><span data-stu-id="d9357-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="d9357-111">Ele demonstra como criar um arquivo de cabeçalho que pode ser compilado condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="d9357-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




