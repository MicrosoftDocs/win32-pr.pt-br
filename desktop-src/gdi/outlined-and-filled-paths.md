---
description: Um aplicativo pode desenhar o contorno de um caminho chamando a função StrokePath, ele pode preencher o interior de um caminho chamando a função FillPath e pode contornar e preencher o caminho chamando a função StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Caminhos de contorno e preenchidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921287"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="12ddb-103">Caminhos de contorno e preenchidos</span><span class="sxs-lookup"><span data-stu-id="12ddb-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="12ddb-104">Um aplicativo pode desenhar o contorno de um caminho chamando a função [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , ele pode preencher o interior de um caminho chamando a função [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) e pode contornar e preencher o caminho chamando a função [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .</span><span class="sxs-lookup"><span data-stu-id="12ddb-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="12ddb-105">Sempre que um aplicativo preenche um caminho, o sistema usa o modo de preenchimento atual do DC.</span><span class="sxs-lookup"><span data-stu-id="12ddb-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="12ddb-106">Um aplicativo pode recuperar esse modo chamando a função [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) e pode definir um novo modo de preenchimento chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="12ddb-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="12ddb-107">Para obter uma descrição dos dois modos de preenchimento, consulte [regiões](regions.md).</span><span class="sxs-lookup"><span data-stu-id="12ddb-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="12ddb-108">A ilustração a seguir mostra a seção cruzada de um objeto criado por um aplicativo CAD (design auxiliado por computador) usando caminhos que foram contornados e preenchidos.</span><span class="sxs-lookup"><span data-stu-id="12ddb-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![ilustração mostrando a exibição de seções cruzadas de um objeto, com várias partes indicadas por padrões de preenchimento diferentes](images/cspth-01.png)

 

 



