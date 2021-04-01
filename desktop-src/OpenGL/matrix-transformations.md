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
# <a name="matrix-transformations"></a><span data-ttu-id="8e255-107">Transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="8e255-107">Matrix Transformations</span></span>

<span data-ttu-id="8e255-108">Os vértices e os normais são transformados pelas matrizes de modelview e de projeção antes de serem usados para produzir uma imagem no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="8e255-108">Vertices and normals are transformed by the modelview and projection matrices before they're used to produce an image in the framebuffer.</span></span> <span data-ttu-id="8e255-109">Use funções como [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**glTranslate \***](gltranslate.md)e [**glScale \***](glscale.md) para compor as transformações desejadas.</span><span class="sxs-lookup"><span data-stu-id="8e255-109">Use functions such as [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix\***](glmultmatrix.md), [**glRotate\***](glrotate.md), [**glTranslate\***](gltranslate.md), and [**glScale\***](glscale.md) to compose the desired transformations.</span></span> <span data-ttu-id="8e255-110">Ou especifique as matrizes diretamente com [**glLoadMatrix \***](glloadmatrix.md) e [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="8e255-110">Or specify matrices directly with [**glLoadMatrix\***](glloadmatrix.md) and [**glLoadIdentity**](glloadidentity.md).</span></span> <span data-ttu-id="8e255-111">Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar as matrizes de modelview e projeção em suas respectivas pilhas.</span><span class="sxs-lookup"><span data-stu-id="8e255-111">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore modelview and projection matrices on their respective stacks.</span></span>

 

 




