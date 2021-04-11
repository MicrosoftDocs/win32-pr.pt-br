---
title: Portando funções do v
description: No íris GL, você usa variações na função v para especificar vértices. A função OpenGL equivalente é glVertex abaixo são exemplos de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Portabilidade do íris GL, vértices
- portando do íris GL, vértices
- portando para OpenGL do íris GL, vértices
- Portabilidade OpenGL do íris GL, vértices
- funções de desenho, vértices
- vértices, portando do íris GL
- Portabilidade do íris GL, funções do v
- portando do íris GL, funções do v
- portando para OpenGL do íris GL, funções do v
- Portabilidade OpenGL do íris GL, funções do v
- funções de desenho, funções do v
- funções do v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292044"
---
# <a name="porting-v-functions"></a>Portando funções do v

No íris GL, você usa variações na função **v** para especificar vértices. A função OpenGL equivalente é [glVertex](glvertex-functions.md): abaixo estão exemplos de **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

A função **glVertex** tem sufixos da mesma maneira que outras chamadas OpenGL. As versões de vetor da chamada assumem matrizes do tamanho adequado como argumentos. Na versão 2-D, z = 0 e w = 1. Na versão 3-D, w = 1.

 

 




