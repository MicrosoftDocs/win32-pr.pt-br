---
title: Controle gráfico OpenGL
description: Controle gráfico OpenGL
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, controle gráfico
- controle gráfico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635935"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="3c246-105">Controle gráfico OpenGL</span><span class="sxs-lookup"><span data-stu-id="3c246-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="3c246-106">O OpenGL fornece um controle bastante direto sobre as operações fundamentais de gráficos de duas e três dimensões.</span><span class="sxs-lookup"><span data-stu-id="3c246-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="3c246-107">Isso inclui a especificação de tais parâmetros como matrizes de transformação, os coeficientes da equação de iluminação, os métodos de suavização e os operadores de atualização de pixel.</span><span class="sxs-lookup"><span data-stu-id="3c246-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="3c246-108">No entanto, ele não fornece um meio para descrever ou modelar objetos geométricos complexos.</span><span class="sxs-lookup"><span data-stu-id="3c246-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="3c246-109">Assim, os comandos OpenGL que você emitir especificam como um determinado resultado deve ser produzido (que procedimento deve ser seguido) em vez do que exatamente esse resultado deve ser semelhante.</span><span class="sxs-lookup"><span data-stu-id="3c246-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="3c246-110">Ou seja, o OpenGL é fundamentalmente um procedimento em vez de descritivo.</span><span class="sxs-lookup"><span data-stu-id="3c246-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="3c246-111">Para entender totalmente como usar o OpenGL, é útil saber a ordem na qual ele realiza suas operações.</span><span class="sxs-lookup"><span data-stu-id="3c246-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




