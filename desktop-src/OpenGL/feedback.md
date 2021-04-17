---
title: Comentários
description: No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores que é copiado para a matriz de comentários.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo de comentários, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105775671"
---
# <a name="feedback-mode"></a><span data-ttu-id="ccb92-104">Modo de comentários</span><span class="sxs-lookup"><span data-stu-id="ccb92-104">Feedback mode</span></span>

<span data-ttu-id="ccb92-105">No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores que é copiado para a matriz de comentários.</span><span class="sxs-lookup"><span data-stu-id="ccb92-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="ccb92-106">Forneça essa matriz com [**glFeedbackBuffer**](glfeedbackbuffer.md), que você deve chamar antes de colocar o OpenGL no modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="ccb92-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="ccb92-107">Cada bloco de valores começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo.</span><span class="sxs-lookup"><span data-stu-id="ccb92-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="ccb92-108">As entradas também são escritas para bitmaps e retângulos de pixel.</span><span class="sxs-lookup"><span data-stu-id="ccb92-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="ccb92-109">Não há garantia de que os valores sejam gravados na matriz de comentários até que você chame [**glRenderMode**](glrendermode.md) para retirar o OpenGL do modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="ccb92-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="ccb92-110">Você pode usar [**glPassThrough**](glpassthrough.md) para fornecer um marcador que é retornado no modo de comentários como se fosse um primitivo.</span><span class="sxs-lookup"><span data-stu-id="ccb92-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




