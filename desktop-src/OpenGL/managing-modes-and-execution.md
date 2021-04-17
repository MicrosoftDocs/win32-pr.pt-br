---
title: Gerenciando modos e execução
description: Gerenciando modos e execução
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754621"
---
# <a name="managing-modes-and-execution"></a>Gerenciando modos e execução

O efeito de muitas funções OpenGL depende se um modo específico está em vigor. As funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) definem tais modos; [**glIsEnabled**](glisenabled.md) determina se um modo específico está definido.

Você pode controlar a execução de funções OpenGL emitidas anteriormente com [**glFinish**](glfinish.md), o que força todas essas funções a serem concluídas, ou [**glFlush**](glflush.md), o que garante que todas essas funções serão preenchidas em um tempo finito.

Em uma implementação específica do OpenGL, você poderá controlar determinados comportamentos com dicas usando [**glHint**](glhint.md). Esses comportamentos são a qualidade das cores e a interpolação de coordenadas de textura; a precisão dos cálculos de neblina; e a qualidade de amostragem de pontos, linhas ou polígonos com alias.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos e referência de execução](modes-and-execution-reference.md)
</dt> </dl>

 

 




