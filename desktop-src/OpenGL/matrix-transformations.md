---
title: Transformações de matriz
description: Os vértices e os normais são transformados pelas matrizes de modelview e de projeção antes de serem usados para produzir uma imagem no framebuffer.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline de processamento OpenGL, matrizes
- matrizes OpenGL
- matriz modelview
- matriz de projeção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159713"
---
# <a name="matrix-transformations"></a>Transformações de matriz

Os vértices e os normais são transformados pelas matrizes de modelview e de projeção antes de serem usados para produzir uma imagem no framebuffer. Use funções como [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**glTranslate \***](gltranslate.md)e [**glScale \***](glscale.md) para compor as transformações desejadas. Ou especifique as matrizes diretamente com [**glLoadMatrix \***](glloadmatrix.md) e [**glLoadIdentity**](glloadidentity.md). Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar as matrizes de modelview e projeção em suas respectivas pilhas.

 

 




