---
title: Transformando coordenadas
description: A biblioteca de utilitário OpenGL (GLU) fornece várias funções de transformação de matriz usadas com frequência.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilitário OpenGL (GLU), funções de transformação de matriz
- GLU (utilitário OpenGL), funções de transformação de matriz
- funções de transformação de matriz OpenGL
- Utilitário OpenGL (GLU), transformando coordenadas
- GLU (utilitário OpenGL), transformando coordenadas
- transformando coordenadas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637047"
---
# <a name="transforming-coordinates"></a>Transformando coordenadas

A biblioteca de utilitário OpenGL (GLU) fornece várias funções de transformação de matriz usadas com frequência. Você pode configurar uma região de exibição ortográfica bidimensional com [**gluOrtho2D**](gluortho2d.md), um volume de exibição de perspectiva padrão usando [**gluPerspective**](gluperspective.md)ou um volume de exibição centralizado em um eyepoint especificado com [**gluLookAt**](glulookat.md). Cada uma dessas funções cria a matriz desejada e a aplica à matriz atual usando [**glMultMatrix**](glmultmatrix.md).

A função [**gluPickMatrix**](glupickmatrix.md) simplifica a seleção de uma matriz de separação criando uma matriz que restringe o desenho a uma pequena região do visor. Se você renderizar novamente a cena no modo de seleção depois que essa matriz tiver sido aplicada, todos os objetos que seriam desenhados próximo ao cursor serão selecionados e as informações sobre elas serão armazenadas no buffer de seleção. Para obter mais informações sobre o modo de seleção, consulte "realizando seleção e comentários" [executando a seleção e os comentários](performing-selection-and-feedback.md).

Para determinar onde na janela um objeto está sendo desenhado, use [**gluProject**](gluproject.md), que converte as coordenadas de objeto especificadas *objx*, *objy* e *objz* em coordenadas de janela usando *modelMatrix*, *projMatrix* e *viewport*. O resultado é armazenado em *Winx*, *winy* e *WINZ*. Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro. Se a função falhar, o valor de retorno será GL \_ false.

A função [**gluUnProject**](gluunproject.md) executa a conversão inversa: transforma a janela especificada coordena *Winx*, *winy* e *WINZ* em coordenadas de objeto usando *modelMatrix*, *projMatrix* e *viewport*. O resultado é armazenado em *objx*, *objy* e *objz*. Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro. Se a função falhar, o valor de retorno será GL \_ false.

 

 




