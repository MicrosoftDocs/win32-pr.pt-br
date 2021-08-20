---
title: Portando código de modo MSINGLE
description: O OpenGL não tem equivalente para MSINGLE, modo de matriz única.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Portação IRIS GL, modo MSINGLE
- portando de IRIS GL, modo MSINGLE
- portando para OpenGL do IRIS GL, modo MSINGLE
- Portação openGL de IRIS GL, modo MSINGLE
- Modo MSINGLE
- Portação IRIS GL, modo de matriz única
- portando do IRIS GL, modo de matriz única
- portando para OpenGL do IRIS GL, modo de matriz única
- Portação openGL do IRIS GL, modo de matriz única
- modo de matriz única
- modo de matriz dupla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132385"
---
# <a name="porting-msingle-mode-code"></a>Portando código de modo MSINGLE

O OpenGL não tem equivalente para **MSINGLE,** modo de matriz única. Embora o uso desse modo tenha sido desacentado, ele é o padrão para IRIS GL. Se o programa IRIS GL usar o modo de matriz única, você precisará reescrevê-lo para usar apenas o modo de matriz dupla. O OpenGL está sempre no modo de matriz dupla e está inicialmente no modo GL \_ MODELVIEW.

A maioria dos códigos IRIS GL no modo MSINGLE tem esta aparência:

``` syntax
projectionmatrix();
```

em *que projectionmatrix* é um de: **orto ,** **orto2**, **perspectiva** ou **janela**. Para fazer a portabilidade para OpenGL, substitua a **função MSINGLE** *-mode projectionmatrix* por:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




