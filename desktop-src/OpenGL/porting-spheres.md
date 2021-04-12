---
title: Portando para cá
description: Ao portar para o OpenGL, tenha os seguintes pontos em mente
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portabilidade do íris GL,
- portando do íris GL,
- portando para OpenGL do íris GL,
- Portabilidade OpenGL do íris GL,
- funções de desenho,
- esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364171"
---
# <a name="porting-spheres"></a>Portando para cá

Ao portar para o OpenGL, tenha em mente os seguintes pontos:

-   Você não pode controlar o tipo de primitivas usadas para desenhar a esfera. Você pode controlar a precisão do desenho de outra maneira: Use os parâmetros Slices e Stacks. As fatias são longitudinal; as pilhas são latitudinais.
-   As difiram são desenhadas centralizadas na origem. Em vez de especificar o local, como você faz com a função **sphdraw** do íris GL, preceda uma chamada para a função [**gluSphere**](glusphere.md) do Glu com uma tradução.
-   A biblioteca de Sphere ainda não está disponível para OpenGL.

A tabela a seguir lista as funções do íris GL para desenhar por meio das suas funções GLU equivalentes, quando disponíveis.



| Função GL de íris | Função GLU                                 | Significado                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Cria um novo objeto de esfera.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Exclui o objeto de esfera e a memória livre usada.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Desenha uma esfera.                               |
| **sphmode**      |                                              | Define os atributos de Sphere.                       |
| **sphrotmatrix** |                                              | Controla a orientação da esfera.                  |
| **sphgnpolys**   |                                              | Retorna o número de polígonos na esfera atual. |



 

??

 

 




