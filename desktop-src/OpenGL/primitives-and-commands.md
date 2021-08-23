---
title: Primitivos e comandos
description: Primitivos e comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitivos
- OpenGL, comandos
- primitivos OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0729b71e9c25abf22045884910fcec3780d50aff2fe94dbe485f83f640cdeced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888056"
---
# <a name="primitives-and-commands"></a>Primitivos e comandos

O OpenGL desenha *pontos primitivos,* segmentos de linha ou polígonossubject para vários modos selecionáveis. Você pode controlar modos independentemente um do outro. Ou seja, definir um modo não afeta se outros modos são definidos (embora muitos modos possam interagir para determinar o que eventualmente termina no framebuffer). Para especificar primitivos, definir modos e executar outras operações do OpenGL, você emitirá comandos na forma de chamadas de função.

Os primitivos são definidos por um grupo de um ou mais *vértices*. Um vértice define um ponto, um ponto de extremidade de uma linha ou um canto de um polígono em que duas bordas se encontram. Os dados (que consistem em coordenadas de vértice, cores, normais, coordenadas de textura e sinalizadores de borda) estão associados a um vértice e cada vértice e seus dados associados são processados independentemente, na ordem e da mesma maneira. As únicas exceções a essa regra são casos em que o grupo de vértices deve ser recortado para que um primitivo específico se ajuste a uma região especificada. Nesse caso, os dados de vértice podem ser modificados e novos vértices criados. O tipo de recorte depende de qual primitivo o grupo de vértices representa.

Os comandos são sempre processados na ordem em que são recebidos, embora possa haver um atraso indeterminado antes que um comando entre em vigor. Isso significa que cada primitivo é desenhado completamente antes que qualquer comando subsequente entre em vigor. Isso também significa que os comandos de consulta de estado retornam dados consistentes com a execução completa de todos os comandos OpenGL emitidos anteriormente.

 

 




