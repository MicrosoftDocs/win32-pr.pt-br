---
title: Portando arcos e círculos
description: Com o OpenGL, arcos e círculos preenchidos são desenhados com as mesmas chamadas como arcos e círculos não preenchidos. A tabela a seguir lista as funções de arco e de círculo da íris GL e suas funções OpenGL (GLU) equivalentes.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Portabilidade do íris GL, arcos
- portando do íris GL, arcos
- portando para OpenGL do íris GL, arcos
- Portabilidade do OpenGL do íris GL, arcos
- funções de desenho, arcos
- Portabilidade do íris GL, círculos
- portando do íris GL, círculos
- portando para OpenGL do íris GL, círculos
- Portabilidade OpenGL do íris GL, círculos
- funções de desenho, círculos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364425"
---
# <a name="porting-arcs-and-circles"></a>Portando arcos e círculos

Com o OpenGL, arcos e círculos preenchidos são desenhados com as mesmas chamadas como arcos e círculos não preenchidos. A tabela a seguir lista as funções de arco e de círculo da íris GL e suas funções OpenGL (GLU) equivalentes.



| Função GL de íris | Função OpenGL                          | Significado                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | Desenha um arco.           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | Desenha um círculo ou disco. |



 

Você pode fazer algumas coisas com arcos e círculos OpenGL que não pode fazer com o íris GL. O OpenGL chama arcos e círculos, discos e discos parciais, respectivamente.

Ao portar arcos e círculos, mantenha os seguintes pontos sobre o OpenGL em mente:

-   Os ângulos são medidos em graus e não em décimos de graus.
-   O ângulo inicial é medido a partir do eixo y positivo e não do eixo x.
-   O ângulo de flecha agora está no sentido horário, em vez de no sentido anti-horário.

??

 

 




