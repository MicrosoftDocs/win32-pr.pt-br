---
title: Introdução ao OpenGL
description: Introdução ao OpenGL
ms.assetid: 8fe214a9-f071-470b-ac72-182a7bd54fbd
keywords:
- OpenGL, introdução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cece636e51348288e587116bf13f95696b93ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916139"
---
# <a name="introduction-to-opengl"></a><span data-ttu-id="edf9e-104">Introdução ao OpenGL</span><span class="sxs-lookup"><span data-stu-id="edf9e-104">Introduction to OpenGL</span></span>

<span data-ttu-id="edf9e-105">Como uma interface de software para hardware de gráficos, a principal finalidade do OpenGL é renderizar objetos de duas e três dimensões em um framebuffer.</span><span class="sxs-lookup"><span data-stu-id="edf9e-105">As a software interface for graphics hardware, the main purpose of OpenGL is to render two- and three-dimensional objects into a framebuffer.</span></span> <span data-ttu-id="edf9e-106">Esses objetos são descritos como sequências de vértices (que definem objetos geométricos) ou pixels (que definem imagens).</span><span class="sxs-lookup"><span data-stu-id="edf9e-106">These objects are described as sequences of vertices (that define geometric objects) or pixels (that define images).</span></span> <span data-ttu-id="edf9e-107">O OpenGL executa vários processos sobre esses dados para convertê-los em pixels para formar a imagem final desejada no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="edf9e-107">OpenGL performs several processes on this data to convert it to pixels to form the final desired image in the framebuffer.</span></span>

<span data-ttu-id="edf9e-108">Os tópicos a seguir apresentam uma visão global de como o OpenGL funciona:</span><span class="sxs-lookup"><span data-stu-id="edf9e-108">The following topics present a global view of how OpenGL works:</span></span>

-   <span data-ttu-id="edf9e-109">[Primitivos e comandos](primitives-and-commands.md) discute pontos, segmentos de linha e polígonos como as unidades básicas de desenho; e o processamento de comandos.</span><span class="sxs-lookup"><span data-stu-id="edf9e-109">[Primitives and Commands](primitives-and-commands.md) discusses points, line segments, and polygons as the basic units of drawing; and the processing of commands.</span></span>
-   <span data-ttu-id="edf9e-110">O [controle gráfico OpenGL](opengl-graphic-control.md) descreve quais operações gráficas do OpenGL controlam e quais não controlam.</span><span class="sxs-lookup"><span data-stu-id="edf9e-110">[OpenGL Graphic Control](opengl-graphic-control.md) describes which graphic operations OpenGL controls and which it does not control.</span></span>
-   <span data-ttu-id="edf9e-111">O [modelo de execução](execution-model.md) discute o modelo de cliente/servidor para interpretar comandos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="edf9e-111">[Execution Model](execution-model.md) discusses the client/server model for interpreting OpenGL commands.</span></span>
-   <span data-ttu-id="edf9e-112">A [operação OpenGL básica](basic-opengl-operation.md) fornece uma descrição de alto nível de como o OpenGL processa os dados para produzir uma imagem correspondente no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="edf9e-112">[Basic OpenGL Operation](basic-opengl-operation.md) gives a high-level description of how OpenGL processes data to produce a corresponding image in the framebuffer.</span></span>
-   <span data-ttu-id="edf9e-113">Os [nomes das funções OpenGL](opengl-function-names.md) descrevem as convenções de nomenclatura usadas no OpenGL.</span><span class="sxs-lookup"><span data-stu-id="edf9e-113">[OpenGL Function Names](opengl-function-names.md) describes the naming conventions used in OpenGL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edf9e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edf9e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf9e-115">Pipeline de processamento OpenGL</span><span class="sxs-lookup"><span data-stu-id="edf9e-115">OpenGL Processing Pipeline</span></span>](opengl-processing-pipeline.md)
</dt> <dt>

[<span data-ttu-id="edf9e-116">Usando avaliadores</span><span class="sxs-lookup"><span data-stu-id="edf9e-116">Using Evaluators</span></span>](using-evaluators.md)
</dt> <dt>

[<span data-ttu-id="edf9e-117">Executando a seleção e os comentários</span><span class="sxs-lookup"><span data-stu-id="edf9e-117">Performing Selection and Feedback</span></span>](performing-selection-and-feedback.md)
</dt> <dt>

[<span data-ttu-id="edf9e-118">Usando listas de exibição</span><span class="sxs-lookup"><span data-stu-id="edf9e-118">Using Display Lists</span></span>](using-display-lists.md)
</dt> <dt>

[<span data-ttu-id="edf9e-119">Gerenciando modos e execução</span><span class="sxs-lookup"><span data-stu-id="edf9e-119">Managing Modes and Execution</span></span>](managing-modes-and-execution.md)
</dt> <dt>

[<span data-ttu-id="edf9e-120">Obtendo informações de estado</span><span class="sxs-lookup"><span data-stu-id="edf9e-120">Obtaining State Information</span></span>](obtaining-state-information.md)
</dt> <dt>

[<span data-ttu-id="edf9e-121">Biblioteca de utilitário OpenGL</span><span class="sxs-lookup"><span data-stu-id="edf9e-121">OpenGL Utility Library</span></span>](opengl-utility-library.md)
</dt> </dl>

 

 




