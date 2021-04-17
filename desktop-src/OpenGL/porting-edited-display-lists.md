---
title: Portando listas de exibição editadas
description: Embora não seja possível editar listas de exibição OpenGL, você pode obter resultados semelhantes aninhando listas de exibição e, em seguida, destruindo e criando novas versões das sublistas.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Portabilidade do íris GL, listas de exibição
- portando do íris GL, listas de exibição
- portando para OpenGL do íris GL, listas de exibição
- Portabilidade OpenGL do íris GL, listas de exibição
- Exibir listas, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757099"
---
# <a name="porting-edited-display-lists"></a>Portando listas de exibição editadas

Embora não seja possível editar listas de exibição OpenGL, você pode obter resultados semelhantes aninhando listas de exibição e, em seguida, destruindo e criando novas versões das sublistas. Por exemplo:

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




