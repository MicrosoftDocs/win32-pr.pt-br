---
title: Portando o código do modo MSINGLE
description: O OpenGL não tem equivalente para o modo MSINGLE, de matriz única.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Portabilidade do íris GL, modo MSINGLE
- portando do íris GL, modo MSINGLE
- portando para OpenGL do íris GL, modo MSINGLE
- Portabilidade OpenGL do íris GL, modo MSINGLE
- Modo de MSINGLE
- Portabilidade do íris GL, modo de matriz única
- portando do íris GL, modo de matriz única
- portando para OpenGL do íris GL, modo de matriz única
- Portabilidade OpenGL do íris GL, modo de matriz única
- modo de matriz única
- modo de matriz dupla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364177"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="f4f48-114">Portando o código do modo MSINGLE</span><span class="sxs-lookup"><span data-stu-id="f4f48-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="f4f48-115">O OpenGL não tem equivalente para o modo **MSINGLE**, de matriz única.</span><span class="sxs-lookup"><span data-stu-id="f4f48-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="f4f48-116">Embora o uso desse modo tenha sido desencorajado, ele é o padrão para o íris GL.</span><span class="sxs-lookup"><span data-stu-id="f4f48-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="f4f48-117">Se o seu programa de íris GL usar o modo de matriz única, você precisará regravá-lo para usar apenas o modo de matriz dupla.</span><span class="sxs-lookup"><span data-stu-id="f4f48-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="f4f48-118">O OpenGL está sempre no modo de matriz dupla e está inicialmente no \_ modo MODELVIEW GL.</span><span class="sxs-lookup"><span data-stu-id="f4f48-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="f4f48-119">A maioria dos códigos GL do íris no modo MSINGLE é semelhante a:</span><span class="sxs-lookup"><span data-stu-id="f4f48-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="f4f48-120">em que *ProjectionMatrix* é uma das **: Ortho**, **ortho2**, **Perspective** ou **Window**.</span><span class="sxs-lookup"><span data-stu-id="f4f48-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="f4f48-121">Para porta para OpenGL, substitua a função *ProjectionMatrix* do modo **MSINGLE** por:</span><span class="sxs-lookup"><span data-stu-id="f4f48-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




