---
title: Transformações de matriz
description: Vértices e normais são transformados pela modelview e matrizes de projeção antes que sejam usados para produzir uma imagem no framebuffer.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline de processamento openGL, matrizes
- matrizes OpenGL
- matriz modelview
- matriz de projeção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937315"
---
# <a name="matrix-transformations"></a>Transformações de matriz

Vértices e normais são transformados pela modelview e matrizes de projeção antes que sejam usados para produzir uma imagem no framebuffer. Use funções como [**glMatrixMode**](glmatrixmode.md), [ * *\* glMultMatrix* _](glmultmatrix.md), [_*glRotate, \**_](glrotate.md) [_*glTranslate \**_](gltranslate.md)e [_*glScale \**_](glscale.md) para compor as transformações desejadas. Ou especifique matrizes diretamente com [_*glLoadMatrix \**_](glloadmatrix.md) e [_ *glLoadIdentity* *](glloadidentity.md). Use [**glPushMatrix e**](glpushmatrix.md) [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar modelview e matrizes de projeção em suas respectivas pilhas.

 

 




