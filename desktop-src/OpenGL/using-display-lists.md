---
title: Usando listas de exibição
description: Usando listas de exibição
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, exibir listas
- Exibir listas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822468"
---
# <a name="using-display-lists"></a><span data-ttu-id="bb541-105">Usando listas de exibição</span><span class="sxs-lookup"><span data-stu-id="bb541-105">Using Display Lists</span></span>

<span data-ttu-id="bb541-106">Uma lista de exibição é um grupo de funções OpenGL que foi armazenado para execução subsequente.</span><span class="sxs-lookup"><span data-stu-id="bb541-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="bb541-107">A função [**glNewList**](glnewlist.md) começa a criação de uma lista de exibição e a [**glEndList**](glendlist.md) a encerra.</span><span class="sxs-lookup"><span data-stu-id="bb541-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="bb541-108">Com poucas exceções, as funções OpenGL chamadas entre **glNewList** e **glEndList** são acrescentadas à lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="bb541-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="bb541-109">(Consulte **glNewList** para obter uma lista das funções que você não pode armazenar e executar de dentro de uma lista de exibição.) Para disparar a execução de uma lista ou conjunto de listas, use [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) e forneça o número de identificação de uma lista ou listas específicas.</span><span class="sxs-lookup"><span data-stu-id="bb541-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="bb541-110">Você gerencia os índices usados para identificar listas de exibição com [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)e [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="bb541-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="bb541-111">Para excluir um conjunto de listas de exibição, use [**glDeleteLists**](gldeletelists.md).</span><span class="sxs-lookup"><span data-stu-id="bb541-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb541-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb541-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb541-113">Referência de listas de exibição</span><span class="sxs-lookup"><span data-stu-id="bb541-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




