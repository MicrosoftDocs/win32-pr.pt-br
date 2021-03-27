---
description: Um aplicativo pode converter um caminho em uma região chamando a função PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversão de caminhos em regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661625"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="7b6bf-103">Conversão de caminhos em regiões</span><span class="sxs-lookup"><span data-stu-id="7b6bf-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="7b6bf-104">Um aplicativo pode converter um caminho em uma região chamando a função [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) .</span><span class="sxs-lookup"><span data-stu-id="7b6bf-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="7b6bf-105">Como [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), o **PathToRegion** é útil na criação de efeitos gráficos especiais.</span><span class="sxs-lookup"><span data-stu-id="7b6bf-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="7b6bf-106">Por exemplo, não há funções que permitam a um aplicativo deslocar um caminho; no entanto, há uma função que permite que um aplicativo offset uma região ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span><span class="sxs-lookup"><span data-stu-id="7b6bf-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="7b6bf-107">Usando o **PathToRegion** , um aplicativo pode criar o efeito de animar uma forma complexa criando um caminho que define a forma, convertendo o caminho em uma região (chamando **PathToRegion**) e, em seguida, pintando, movendo e apagando a região (chamando funções em uma seqüência, como [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** e **FillRgn**).</span><span class="sxs-lookup"><span data-stu-id="7b6bf-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



