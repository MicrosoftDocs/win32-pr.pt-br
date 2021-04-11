---
title: Seleção
description: A seleção retorna o conteúdo atual da pilha de nomes, que é uma matriz de nomes com valores inteiros.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modo de seleção OpenGL
- acertos de seleção OpenGL
- registros de clique OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292357"
---
# <a name="selection"></a>Seleção

A seleção retorna o conteúdo atual da pilha de nomes, que é uma matriz de nomes com valores inteiros. Você atribui os nomes e cria a pilha de nomes dentro do código de modelagem que especifica a geometria de objetos que você deseja desenhar. Em seguida, no modo de seleção, sempre que um primitivo intercepta o volume do clipe, ocorre uma ocorrência de seleção. O registro de acesso, que é gravado na matriz de seleção que você forneceu com [**glSelectBuffer**](glselectbuffer.md), contém informações sobre o conteúdo da pilha de nomes no momento da visita.

> [!Note]  
> Chame [**glSelectBuffer**](glselectbuffer.md) antes de colocar o OpenGL no modo de seleção com [**glRenderMode**](glrendermode.md). Não há garantia de que todo o conteúdo da pilha de nomes seja retornado até que você chame **glRenderMode** para retirar o OpenGL do modo de seleção.

 

Manipule a pilha de nomes com [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)e [**glPopName**](glpopname.md). Você também pode usar [**gluPickMatrix**](glupickmatrix.md) para seleção.

 

 




