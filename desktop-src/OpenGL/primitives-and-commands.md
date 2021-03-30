---
title: Primitivos e comandos
description: Primitivos e comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitivos
- OpenGL, comandos
- primitivas OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635555"
---
# <a name="primitives-and-commands"></a>Primitivos e comandos

O OpenGL desenha pontos *primitivos* , segmentos de linha ou polygonssubject para vários modos selecionáveis. Você pode controlar modos de forma independente um do outro. Ou seja, definir um modo não afeta se outros modos estão definidos (embora muitos modos possam interagir para determinar o que eventualmente acaba no framebuffer). Para especificar primitivos, definir modos e executar outras operações OpenGL, você emite comandos na forma de chamadas de função.

Os primitivos são definidos por um grupo de um ou mais *vértices*. Um vértice define um ponto, um ponto de extremidade de uma linha ou um canto de um polígono onde duas bordas se encontram. Os dados (que consistem em coordenadas de vértice, cores, normais, coordenadas de textura e sinalizadores de borda) são associados a um vértice, e cada vértice e seus dados associados são processados de forma independente, em ordem, e da mesma maneira. As únicas exceções a essa regra são casos em que o grupo de vértices deve ser recortado para que um primitivo específico caiba em uma região especificada. Nesse caso, os dados de vértice podem ser modificados e novos vértices criados. O tipo de recorte depende de qual primitiva o grupo de vértices representa.

Os comandos são sempre processados na ordem em que são recebidos, embora possa haver um atraso indeterminado antes de um comando entrar em vigor. Isso significa que cada primitivo é desenhado completamente antes de qualquer comando subsequente entrar em vigor. Isso também significa que os comandos de consulta de estado retornam dados consistentes com a execução completa de todos os comandos OpenGL emitidos anteriormente.

 

 




