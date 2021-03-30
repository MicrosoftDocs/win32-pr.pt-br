---
title: Teste de estêncil
description: O teste de estêncil descarta condicionalmente um fragmento com base no resultado de uma comparação entre o valor no buffer do estêncil e um valor de referência.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Pipeline de processamento de OpenGL, teste de estêncil
- OpenGL de teste de estêncil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637045"
---
# <a name="stencil-test"></a><span data-ttu-id="bf0db-105">Teste de estêncil</span><span class="sxs-lookup"><span data-stu-id="bf0db-105">Stencil Test</span></span>

<span data-ttu-id="bf0db-106">O teste de estêncil descarta condicionalmente um fragmento com base no resultado de uma comparação entre o valor no buffer do estêncil e um valor de referência.</span><span class="sxs-lookup"><span data-stu-id="bf0db-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="bf0db-107">A função [**glStencilFunc**](glstencilfunc.md) especifica a função de comparação e o valor de referência.</span><span class="sxs-lookup"><span data-stu-id="bf0db-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="bf0db-108">Se o fragmento passa ou falha no teste de estêncil, o valor no buffer de estêncil é modificado de acordo com as instruções especificadas com [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="bf0db-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




