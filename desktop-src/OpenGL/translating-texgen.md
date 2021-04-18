---
title: Convertendo texgen
description: A função texgen do íris GL é convertida em glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
- Portabilidade do íris GL, texgen
- portando do íris GL, texgen
- portando para OpenGL do íris GL, texgen
- Portabilidade OpenGL do íris GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757097"
---
# <a name="translating-texgen"></a>Convertendo texgen

A função **texgen** do íris GL é convertida em [glTexGen](gltexgen-functions.md) para OpenGL.

Com o íris GL, você chama **texgen** duas vezes: uma vez para definir o modo e a equação do plano simultaneamente, e uma vez para habilitar a geração da coordenada de textura. Por exemplo:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Com o OpenGL, você faz três chamadas: dois para **glTexGen** (uma vez para definir o modo e uma vez para definir a equação de plano) e um para [**glEnable**](glenable.md). Por exemplo, o OpenGL equivalente ao código de íris GL acima é:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



A tabela a seguir lista os nomes de coordenadas de textura do íris GL e seus equivalentes em OpenGL.



| Coordenada de textura do íris GL | Coordenada de textura OpenGL | argumento glEnable   |
|----------------------------|---------------------------|---------------------|
| \_S TX                      | \_S GL                     | S do GL \_ Texture \_ Gen \_ |
| T de TX \_                      | GL \_ T                     | \_geração de textura de Texture GL \_ \_ |
| \_R TX                      | GL \_ R                     | o GL de \_ Texture \_ Gen \_ R |
| TX \_ Q                      | GL \_ Q                     | GL \_ Texture \_ Gen \_ Q |



 

A tabela a seguir lista os modos de geração de textura do íris GL e seus modos de textura e nomes de plano do OpenGL equivalentes.



| Modo de textura do íris GL | Modo de textura OpenGL | Nome do plano OpenGL |
|----------------------|---------------------|-------------------|
| TG \_ linear           | \_objeto GL \_ linear  | \_plano de objeto GL \_ |
| delimitação de TG \_          | olho do GL \_ \_ linear     | \_plano de olho GL \_    |
| TG \_ SPHEREMAP        | \_mapa de esfera GL \_     |                   |



 

 

 




