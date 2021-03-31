---
title: Nomes de função OpenGL
description: Muitas funções OpenGL são variações umas das outras, diferentes principalmente nos tipos de dados de seus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomes de função
- nomes de função OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635937"
---
# <a name="opengl-function-names"></a><span data-ttu-id="c7ef1-105">Nomes de função OpenGL</span><span class="sxs-lookup"><span data-stu-id="c7ef1-105">OpenGL Function Names</span></span>

<span data-ttu-id="c7ef1-106">Muitas funções OpenGL são variações umas das outras, diferentes principalmente nos tipos de dados de seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="c7ef1-107">Algumas funções diferem no número de argumentos relacionados e se esses argumentos podem ser especificados como um vetor ou devem ser especificados separadamente em uma lista.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="c7ef1-108">Por exemplo, se você usar a função **glVertex2f** , será necessário fornecer coordenadas x e y como números de ponto flutuante de 32 bits; com o **glVertex3sv**, você deve fornecer uma matriz de três valores inteiros curtos (16 bits) para x, y e z.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="c7ef1-109">Somente o nome base da função é usado nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="c7ef1-110">Um asterisco indica que pode haver mais para o nome da função real do que é mostrado.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="c7ef1-111">Por exemplo, [glVertex \*](glvertex-functions.md) significa todas as variações da função que você usa para especificar vértices: **glVertex2d**, **glVertex2f**, **glVertex2i** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="c7ef1-112">O efeito de uma função OpenGL pode variar dependendo se determinados modos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="c7ef1-113">Por exemplo, você precisa habilitar a iluminação se as funções relacionadas à iluminação forem produzir um objeto aceso adequadamente.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="c7ef1-114">Para habilitar um modo específico, use a função [**glEnable**](glenable.md) e forneça a constante apropriada para identificar o modo (por exemplo, \_ iluminação GL).</span><span class="sxs-lookup"><span data-stu-id="c7ef1-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="c7ef1-115">Para desabilitar um modo, use [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="c7ef1-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="c7ef1-116">Consulte **glEnable** para obter uma lista completa dos modos que podem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="c7ef1-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




