---
title: Executando a seleção e os comentários
description: Executando a seleção e os comentários
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, seleção
- OpenGL, comentários
- OpenGL, renderização
- modo de seleção OpenGL
- modo de comentários OpenGL
- modo de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292188"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="e3597-109">Executando a seleção e os comentários</span><span class="sxs-lookup"><span data-stu-id="e3597-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="e3597-110">A seleção, os comentários e a renderização são modos mutuamente exclusivos de operação.</span><span class="sxs-lookup"><span data-stu-id="e3597-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="e3597-111">A renderização é o modo padrão normal durante o qual os fragmentos são produzidos pela rasterização.</span><span class="sxs-lookup"><span data-stu-id="e3597-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="e3597-112">Nos modos de seleção e de comentários, nenhum fragmento é produzido; Portanto, nenhuma modificação framebuffer ocorre.</span><span class="sxs-lookup"><span data-stu-id="e3597-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="e3597-113">No modo de seleção, você pode determinar quais primitivos serão desenhados em alguma região de uma janela; no modo de comentários, as informações sobre primitivas que serão rasterizadas são alimentadas de volta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3597-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="e3597-114">Você seleciona entre esses três modos com [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="e3597-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="e3597-115">Seleção</span><span class="sxs-lookup"><span data-stu-id="e3597-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="e3597-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3597-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="e3597-117">Referência de seleção e comentários</span><span class="sxs-lookup"><span data-stu-id="e3597-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




