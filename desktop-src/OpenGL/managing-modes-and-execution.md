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
# <a name="managing-modes-and-execution"></a><span data-ttu-id="52fad-104">Gerenciando modos e execução</span><span class="sxs-lookup"><span data-stu-id="52fad-104">Managing Modes and Execution</span></span>

<span data-ttu-id="52fad-105">O efeito de muitas funções OpenGL depende se um modo específico está em vigor.</span><span class="sxs-lookup"><span data-stu-id="52fad-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="52fad-106">As funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) definem tais modos; [**glIsEnabled**](glisenabled.md) determina se um modo específico está definido.</span><span class="sxs-lookup"><span data-stu-id="52fad-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="52fad-107">Você pode controlar a execução de funções OpenGL emitidas anteriormente com [**glFinish**](glfinish.md), o que força todas essas funções a serem concluídas, ou [**glFlush**](glflush.md), o que garante que todas essas funções serão preenchidas em um tempo finito.</span><span class="sxs-lookup"><span data-stu-id="52fad-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="52fad-108">Em uma implementação específica do OpenGL, você poderá controlar determinados comportamentos com dicas usando [**glHint**](glhint.md).</span><span class="sxs-lookup"><span data-stu-id="52fad-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="52fad-109">Esses comportamentos são a qualidade das cores e a interpolação de coordenadas de textura; a precisão dos cálculos de neblina; e a qualidade de amostragem de pontos, linhas ou polígonos com alias.</span><span class="sxs-lookup"><span data-stu-id="52fad-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52fad-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52fad-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52fad-111">Modos e referência de execução</span><span class="sxs-lookup"><span data-stu-id="52fad-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




