---
title: Portando defs, associações e conjuntos
description: Portando defs, associações e conjuntos
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Portabilidade do íris GL, definições
- portando do íris GL, definições
- portando para OpenGL do íris GL, definições
- Portabilidade OpenGL do íris GL, definições
- Portabilidade do íris GL, associações
- portando do íris GL, associações
- portando para OpenGL do íris GL, associações
- Portabilidade OpenGL do íris GL, associações
- Portabilidade do íris GL, conjuntos
- portando do íris GL, conjuntos
- portando para OpenGL do íris GL, conjuntos
- Portabilidade OpenGL do íris GL, conjuntos
- definitions
- associa
- conjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a4c3776d3e5eb8000a4e81578bb5df95658a37e0793944a9cda6923fc7a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132658"
---
# <a name="porting-defs-binds-and-sets"></a>Portando defs, associações e conjuntos

O OpenGL não tem tabelas de definições armazenadas; Você não pode definir modelos de iluminação, material, texturas, estilos de linha ou padrões como objetos separados como você pode no íris GL. Portanto, o OpenGL não tem equivalentes diretos às seguintes funções do íris GL:

-   **Imdef** e **imassociação**
-   **tevdef** e **tevbind**
-   **textdef** e **textbind**
-   **refinastyle** e **SetStyle**
-   **defpattern** e **setpattern**

Você pode usar as listas de exibição do OpenGL para imitar o mecanismo de Def/BIND GL da íris. Por exemplo, aqui está uma definição de material no íris GL:


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



O exemplo de código OpenGL a seguir define o mesmo material em uma lista de exibição que é referenciada pelo número da lista definido pelo **mymaterial**.


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




