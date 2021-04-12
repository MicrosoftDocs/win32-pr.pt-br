---
title: Usando objetos de mosaico
description: Como um polígono complexo está sendo descrito e mosaico, ele requer dados associados, como os vértices, as bordas e as funções de retorno de chamada.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilitário OpenGL (GLU), objetos de mosaico
- GLU (utilitário OpenGL), objetos de mosaico
- objetos de mosaico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291988"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="2a82e-106">Usando objetos de mosaico</span><span class="sxs-lookup"><span data-stu-id="2a82e-106">Using Tessellation Objects</span></span>

<span data-ttu-id="2a82e-107">Como um polígono complexo está sendo descrito e mosaico, ele requer dados associados, como os vértices, as bordas e as funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2a82e-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="2a82e-108">Todos esses dados estão vinculados a um único objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="2a82e-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="2a82e-109">Para incluí um polígono, primeiro você usa a função [**gluNewTess**](glunewtess.md) , que cria um novo objeto de mosaico e retorna um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="2a82e-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="2a82e-110">Um ponteiro nulo será retornado se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="2a82e-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="2a82e-111">Se você não precisar mais de um objeto de mosaico, poderá excluí-lo e liberar toda a memória associada com [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="2a82e-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="2a82e-112">Você pode reutilizar um único objeto de mosaico para todos os seus mosaicos.</span><span class="sxs-lookup"><span data-stu-id="2a82e-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="2a82e-113">Esse objeto é necessário apenas porque as funções de biblioteca podem precisar fazer seus próprios mosaicos, e eles devem ser capazes de fazer isso sem interferir em qualquer mosaico que seu programa esteja executando.</span><span class="sxs-lookup"><span data-stu-id="2a82e-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="2a82e-114">Vários objetos de mosaico também são úteis se você quiser usar diferentes conjuntos de retornos de chamada para diferentes mosaicos.</span><span class="sxs-lookup"><span data-stu-id="2a82e-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="2a82e-115">Normalmente, no entanto, você aloca um único objeto de mosaico e o utiliza para todos os mosaicos.</span><span class="sxs-lookup"><span data-stu-id="2a82e-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="2a82e-116">Não há necessidade real de liberá-lo, pois ele usa uma pequena quantidade de memória.</span><span class="sxs-lookup"><span data-stu-id="2a82e-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="2a82e-117">Por outro lado, se você estiver escrevendo uma função de biblioteca que usa o mosaico GLU, tenha cuidado para liberar todos os objetos de mosaico que criar.</span><span class="sxs-lookup"><span data-stu-id="2a82e-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




