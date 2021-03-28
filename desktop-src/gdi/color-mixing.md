---
description: A mistura de cores permite que um aplicativo crie novas cores combinando a cor da caneta ou do pincel com cores na imagem existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Mistura de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091203"
---
# <a name="color-mixing"></a><span data-ttu-id="8c253-103">Mistura de cores</span><span class="sxs-lookup"><span data-stu-id="8c253-103">Color Mixing</span></span>

<span data-ttu-id="8c253-104">A mistura de cores permite que um aplicativo crie novas cores combinando a cor da caneta ou do pincel com cores na imagem existente.</span><span class="sxs-lookup"><span data-stu-id="8c253-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="8c253-105">O aplicativo pode escolher para desenhar a cor da caneta ou do pincel como está (desenhando efetivamente em qualquer imagem existente) ou para misturar a cor com as cores já presentes.</span><span class="sxs-lookup"><span data-stu-id="8c253-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="8c253-106">O modo mix de primeiro plano, às vezes chamado de operação de rasterização binária, determina como essas cores são misturadas.</span><span class="sxs-lookup"><span data-stu-id="8c253-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="8c253-107">Um aplicativo pode mesclar cores, preservando todos os componentes de ambas as cores; mascarar cores, remover ou moderarr componentes que não são comuns; ou exclusivamente mascarar cores, remover ou moderarr componentes comuns.</span><span class="sxs-lookup"><span data-stu-id="8c253-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="8c253-108">Há várias variações nessas operações básicas de mixagem.</span><span class="sxs-lookup"><span data-stu-id="8c253-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="8c253-109">A combinação de cores está sujeita à aproximação de cores.</span><span class="sxs-lookup"><span data-stu-id="8c253-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="8c253-110">Se o resultado da mistura de cores for uma cor que o dispositivo não pode gerar, o sistema aproxima o resultado, usando uma cor que ele pode gerar.</span><span class="sxs-lookup"><span data-stu-id="8c253-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="8c253-111">Se um aplicativo misturar cores diferentes, as cores individuais usadas para criar a cor diquerda serão misturadas e os resultados estarão sujeitos à aproximação de cor.</span><span class="sxs-lookup"><span data-stu-id="8c253-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="8c253-112">Um aplicativo define o modo de combinação de primeiro plano usando a função [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) e recupera o modo atual usando a função [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .</span><span class="sxs-lookup"><span data-stu-id="8c253-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="8c253-113">Embora haja um modo de combinação em segundo plano, esse modo não controla a mistura de cores.</span><span class="sxs-lookup"><span data-stu-id="8c253-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="8c253-114">Em vez disso, especifica se uma cor de plano de fundo é usada ao desenhar linhas com estilo, pincéis hachurados e texto.</span><span class="sxs-lookup"><span data-stu-id="8c253-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



