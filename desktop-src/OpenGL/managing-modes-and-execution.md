---
title: Gerenciando modos e execução
description: Gerenciando modos e execução
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec448fa94c8ed0983be68f8aa1dbbef0974d2e040c4f68b002b026b300406981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553976"
---
# <a name="managing-modes-and-execution"></a>Gerenciando modos e execução

O efeito de muitas funções OpenGL depende se um modo específico está em vigor. As [**funções glEnable**](glenable.md) e [**glDisable**](gldisable.md) configuram esses modos; [**glIsEnabled**](glisenabled.md) determina se um modo específico está definido.

Você pode controlar a execução de funções OpenGL emitidas anteriormente com [**glFinish**](glfinish.md), que força todas essas funções a serem concluídas, ou [**glFlush,**](glflush.md)o que garante que todas essas funções sejam concluídas em um tempo finito.

Em uma implementação específica do OpenGL, você pode controlar determinados comportamentos com dicas usando [**glHint.**](glhint.md) Esses comportamentos são a qualidade da interpolação de coordenadas de cor e textura; a precisão dos cálculos de cálculos de mosca; e a qualidade de amostragem de pontos, linhas ou polígonos antialiasados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos e referência de execução](modes-and-execution-reference.md)
</dt> </dl>

 

 




