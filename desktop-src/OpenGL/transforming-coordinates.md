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
# <a name="transforming-coordinates"></a><span data-ttu-id="4aeb4-109">Transformando coordenadas</span><span class="sxs-lookup"><span data-stu-id="4aeb4-109">Transforming Coordinates</span></span>

<span data-ttu-id="4aeb4-110">A biblioteca de utilitário OpenGL (GLU) fornece várias funções de transformação de matriz usadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="4aeb4-111">Você pode configurar uma região de exibição ortográfica bidimensional com [**gluOrtho2D**](gluortho2d.md), um volume de exibição de perspectiva padrão usando [**gluPerspective**](gluperspective.md)ou um volume de exibição centralizado em um eyepoint especificado com [**gluLookAt**](glulookat.md).</span><span class="sxs-lookup"><span data-stu-id="4aeb4-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="4aeb4-112">Cada uma dessas funções cria a matriz desejada e a aplica à matriz atual usando [**glMultMatrix**](glmultmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4aeb4-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="4aeb4-113">A função [**gluPickMatrix**](glupickmatrix.md) simplifica a seleção de uma matriz de separação criando uma matriz que restringe o desenho a uma pequena região do visor.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="4aeb4-114">Se você renderizar novamente a cena no modo de seleção depois que essa matriz tiver sido aplicada, todos os objetos que seriam desenhados próximo ao cursor serão selecionados e as informações sobre elas serão armazenadas no buffer de seleção.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="4aeb4-115">Para obter mais informações sobre o modo de seleção, consulte "realizando seleção e comentários" [executando a seleção e os comentários](performing-selection-and-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="4aeb4-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="4aeb4-116">Para determinar onde na janela um objeto está sendo desenhado, use [**gluProject**](gluproject.md), que converte as coordenadas de objeto especificadas *objx*, *objy* e *objz* em coordenadas de janela usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="4aeb4-117">O resultado é armazenado em *Winx*, *winy* e *WINZ*.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="4aeb4-118">Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="4aeb4-119">Se a função falhar, o valor de retorno será GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="4aeb4-120">A função [**gluUnProject**](gluunproject.md) executa a conversão inversa: transforma a janela especificada coordena *Winx*, *winy* e *WINZ* em coordenadas de objeto usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="4aeb4-121">O resultado é armazenado em *objx*, *objy* e *objz*.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="4aeb4-122">Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="4aeb4-123">Se a função falhar, o valor de retorno será GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="4aeb4-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 




