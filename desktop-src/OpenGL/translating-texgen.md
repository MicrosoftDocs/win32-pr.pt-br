---
title: Traduzindo o texgen
description: A função IRIS GL é convertida em glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Portação IRIS GL, textura
- portando de IRIS GL, textura
- portando para OpenGL de IRIS GL, textura
- Portação openGL de IRIS GL, textura
- textura
- Portação IRIS GL, texgen
- portando de IRIS GL, texgen
- portando para OpenGL de IRIS GL, texgen
- Portação openGL de IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4280df245b4fce4a9128d4e409a6fbf407075bf7d98fc714314faecc1e242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980457"
---
# <a name="translating-texgen"></a>Traduzindo o texgen

A função IRIS GL **é convertida** em [glTexGen](gltexgen-functions.md) para OpenGL.

Com IRIS GL, você chama **o texgen duas** vezes: uma vez para definir o modo e a equação do plano simultaneamente e uma vez para habilitar a geração de coordenadas de textura. Por exemplo:


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Com o OpenGL, você faz três chamadas: duas para **glTexGen** (uma para definir o modo e outra para definir a equação do plano) e uma para [**glEnable.**](glenable.md) Por exemplo, o equivalente do OpenGL ao código IRIS GL acima é:


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



A tabela a seguir lista os nomes das coordenadas de textura IRIS GL e seus equivalentes openGL.



| Coordenada de textura IRIS GL | Coordenada de textura OpenGL | Argumento glEnable   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | GL \_ TEXTURE \_ GEN \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ TEXTURE \_ GEN \_ T |
| TX \_ R                      | GL \_ R                     | GL \_ TEXTURE \_ GEN \_ R |
| TX \_ Q                      | GL \_ Q                     | GL \_ TEXTURE \_ GEN \_ Q |



 

A tabela a seguir lista os modos de geração de textura IRIS GL e seus modos de textura e nomes de plano equivalentes do OpenGL.



| Modo de textura IRIS GL | Modo de textura OpenGL | Nome do plano OpenGL |
|----------------------|---------------------|-------------------|
| TG \_ LINEAR           | OBJETO GL \_ \_ LINEAR  | PLANO \_ DE \_ OBJETO GL |
| TG \_ VAIR          | GL \_ EYE \_ LINEAR     | PLANO \_ DE OLHO \_ GL    |
| TG \_ SPHEREMAP        | MAPA GL \_ SPHERE \_     |                   |



 

 

 




