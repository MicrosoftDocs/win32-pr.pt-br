---
title: Portando listas de exibição editadas
description: Embora não seja possível editar listas de exibição do OpenGL, você pode obter resultados semelhantes aninhando listas de exibição e, em seguida, destrói e cria novas versões das sublistas.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Portação IRIS GL, listas de exibição
- portando do IRIS GL, listas de exibição
- portando para OpenGL do IRIS GL, listas de exibição
- Portação openGL do IRIS GL, listas de exibição
- listas de exibição, portando do IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13f1630b0560091482d47f85e038d908dcfab202ae772c4d35dc388324b46075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485576"
---
# <a name="porting-edited-display-lists"></a>Portando listas de exibição editadas

Embora não seja possível editar listas de exibição do OpenGL, você pode obter resultados semelhantes aninhando listas de exibição e, em seguida, destrói e cria novas versões das sublistas. Por exemplo:

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

 

 




