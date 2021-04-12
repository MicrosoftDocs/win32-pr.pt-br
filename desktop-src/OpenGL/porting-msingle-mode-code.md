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
# <a name="porting-msingle-mode-code"></a>Portando o código do modo MSINGLE

O OpenGL não tem equivalente para o modo **MSINGLE**, de matriz única. Embora o uso desse modo tenha sido desencorajado, ele é o padrão para o íris GL. Se o seu programa de íris GL usar o modo de matriz única, você precisará regravá-lo para usar apenas o modo de matriz dupla. O OpenGL está sempre no modo de matriz dupla e está inicialmente no \_ modo MODELVIEW GL.

A maioria dos códigos GL do íris no modo MSINGLE é semelhante a:

``` syntax
projectionmatrix();
```

em que *ProjectionMatrix* é uma das **: Ortho**, **ortho2**, **Perspective** ou **Window**. Para porta para OpenGL, substitua a função *ProjectionMatrix* do modo **MSINGLE** por:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




