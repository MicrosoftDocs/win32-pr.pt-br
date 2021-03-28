---
description: Os caminhos são definidos usando unidades lógicas e transformações atuais.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformações de caminhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968086"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="bb0ce-103">Transformações de caminhos</span><span class="sxs-lookup"><span data-stu-id="bb0ce-103">Transformations of Paths</span></span>

<span data-ttu-id="bb0ce-104">Os caminhos são definidos usando unidades lógicas e transformações atuais.</span><span class="sxs-lookup"><span data-stu-id="bb0ce-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="bb0ce-105">(Se a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) tiver sido chamada, as unidades lógicas são unidades mundiais; caso contrário, as unidades lógicas são unidades de página.) Um aplicativo pode usar transformações mundiais para dimensionar, girar, distorcer, traduzir e refletir as linhas e as curvas Bézier que definem um caminho.</span><span class="sxs-lookup"><span data-stu-id="bb0ce-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="bb0ce-106">Uma transformação do mundo dentro de um colchete só afeta as linhas e curvas desenhadas após a definição da transformação.</span><span class="sxs-lookup"><span data-stu-id="bb0ce-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="bb0ce-107">Ele não terá nenhum efeito nessas linhas e curvas que foram desenhadas antes de ser definida.</span><span class="sxs-lookup"><span data-stu-id="bb0ce-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="bb0ce-108">Para obter uma descrição da transformação do mundo, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="bb0ce-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="bb0ce-109">Um aplicativo também pode usar [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para descrever a forma da caneta usada para descrever um caminho se a caneta for uma caneta geométrica.</span><span class="sxs-lookup"><span data-stu-id="bb0ce-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="bb0ce-110">Para obter uma descrição das canetas geométricas, consulte [canetas](pens.md).</span><span class="sxs-lookup"><span data-stu-id="bb0ce-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



