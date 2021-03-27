---
description: Alguns aplicativos fornecem recursos que refletem (ou espelham) objetos desenhados na área do cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967601"
---
# <a name="reflection"></a><span data-ttu-id="f7646-103">Reflexão</span><span class="sxs-lookup"><span data-stu-id="f7646-103">Reflection</span></span>

<span data-ttu-id="f7646-104">Alguns aplicativos fornecem recursos que refletem (ou espelham) objetos desenhados na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f7646-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="f7646-105">Os aplicativos que contêm recursos de reflexão usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir os valores apropriados no espaço mundial para a transformação de espaço em página.</span><span class="sxs-lookup"><span data-stu-id="f7646-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="f7646-106">Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="f7646-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="f7646-107">Os membros eM11 e eM22 do XFORM especificam os componentes de reflexo horizontal e vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f7646-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="f7646-108">A *transformação reflexão* cria uma imagem espelho de um objeto em relação ao eixo x ou y.</span><span class="sxs-lookup"><span data-stu-id="f7646-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="f7646-109">Em suma, a reflexão é apenas uma escala negativa.</span><span class="sxs-lookup"><span data-stu-id="f7646-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="f7646-110">Para produzir uma reflexão horizontal, as coordenadas x são multiplicadas por 1.</span><span class="sxs-lookup"><span data-stu-id="f7646-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="f7646-111">Para produzir uma reflexão vertical, as coordenadas y são multiplicadas por 1.</span><span class="sxs-lookup"><span data-stu-id="f7646-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="f7646-112">A reflexão horizontal pode ser representada pelo seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="f7646-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="f7646-113">em que x é a coordenada x e x ' é o resultado da reflexão.</span><span class="sxs-lookup"><span data-stu-id="f7646-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="f7646-114">A matriz 2-por-2 que produziu a reflexão horizontal contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f7646-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="f7646-115">A reflexão vertical pode ser representada pelo seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="f7646-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="f7646-116">em que y é a coordenada y e y ' é o resultado da reflexão.</span><span class="sxs-lookup"><span data-stu-id="f7646-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="f7646-117">A matriz 2-por-2 que produziu a reflexão vertical contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f7646-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="f7646-118">As operações de reflexão horizontal e de reflexo vertical podem ser combinadas em uma única operação usando a seguinte matriz 2-por-2:</span><span class="sxs-lookup"><span data-stu-id="f7646-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



