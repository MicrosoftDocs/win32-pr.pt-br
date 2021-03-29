---
description: Um objeto GraphicsPath armazena uma sequência de linhas e B&\# 233; ziers.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Nivelamento de caminhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987962"
---
# <a name="flattening-paths"></a><span data-ttu-id="e4053-103">Nivelamento de caminhos</span><span class="sxs-lookup"><span data-stu-id="e4053-103">Flattening Paths</span></span>

<span data-ttu-id="e4053-104">Um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) armazena uma sequência de linhas e uma linhagem de Bézier.</span><span class="sxs-lookup"><span data-stu-id="e4053-104">A [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="e4053-105">Você pode adicionar vários tipos de curvas (elipses, arcos, splines Cardeal) a um caminho, mas cada curva é convertida em uma spline Bézier antes de ser armazenada no caminho.</span><span class="sxs-lookup"><span data-stu-id="e4053-105">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="e4053-106">O nivelamento de um caminho consiste na conversão de cada spline de Bézier no caminho para uma sequência de linhas retas.</span><span class="sxs-lookup"><span data-stu-id="e4053-106">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span>

<span data-ttu-id="e4053-107">Para mesclar um caminho, chame o método [**GraphicsPath:: achata**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) de um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="e4053-107">To flatten a path, call the [**GraphicsPath::Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="e4053-108">O método **GraphicsPath:: achatado** recebe um argumento Flatness que especifica a distância máxima entre o caminho nivelado e o caminho original.</span><span class="sxs-lookup"><span data-stu-id="e4053-108">The **GraphicsPath::Flatten** method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span> <span data-ttu-id="e4053-109">A ilustração a seguir mostra um caminho antes e depois do nivelamento.</span><span class="sxs-lookup"><span data-stu-id="e4053-109">The following illustration shows a path before and after flattening.</span></span>

![ilustração mostrando uma sequência de polilinhas de Bézier conectadas em azul e as linhas correspondentes em vermelho](images/aboutgdip02-art32a.png)

 

 



