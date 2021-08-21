---
title: Esferas de portação
description: Ao portar esferas para OpenGL, lembre-se dos seguintes pontos
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portação IRIS GL, esferas
- portando de IRIS GL,spheres
- portando para OpenGL de IRIS GL,spheres
- Portação openGL de IRIS GL,spheres
- funções de desenho, esferas
- Esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358304"
---
# <a name="porting-spheres"></a>Esferas de portação

Ao portar esferas para OpenGL, lembre-se dos seguintes pontos:

-   Não é possível controlar o tipo de primitivos usados para desenhar a esfera. Você pode controlar a precisão de desenho de outra maneira: use os parâmetros de fatias e pilhas. As fatias são de ; as pilhas são latitudinais.
-   As esferas são desenhadas centralizadas na origem. Em vez de especificar o local, como você faz com a função de **sphdraw** IRIS GL, preceda uma chamada para a função GLU [**gluSphere**](glusphere.md) com uma tradução.
-   A biblioteca sphere ainda não está disponível para OpenGL.

A tabela a seguir lista as funções IRIS GL para esferas de desenho e suas funções GLU equivalentes quando disponíveis.



| Função IRIS GL | Função GLU                                 | Significado                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Cria um novo objeto de esfera.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Exclui o objeto sphere e a memória livre usada.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Desenha uma esfera.                               |
| **sphmode**      |                                              | Define atributos de esfera.                       |
| **sphrotmatrix** |                                              | Controla a orientação da esfera.                  |
| **sphgnpolys**   |                                              | Retorna o número de polígonos na esfera atual. |



 

??

 

 




