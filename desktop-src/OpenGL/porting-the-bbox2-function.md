---
title: Portando a função bbox2
description: Não há nenhum equivalente em OpenGL para a função bbox2 do íris GL.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Portabilidade do íris GL, função bbox2
- portando do íris GL, função bbox2
- portando para OpenGL do íris GL, função bbox2
- Portabilidade OpenGL do íris GL, função bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636568"
---
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="e5ffe-107">Portando a função bbox2</span><span class="sxs-lookup"><span data-stu-id="e5ffe-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="e5ffe-108">Não há nenhum equivalente em OpenGL para a função **bbox2** do íris GL.</span><span class="sxs-lookup"><span data-stu-id="e5ffe-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="e5ffe-109">**Para o código de porta que contém funções bbox2**</span><span class="sxs-lookup"><span data-stu-id="e5ffe-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="e5ffe-110">Crie uma nova lista de exibição (OpenGL) que contenha tudo na lista de exibição equivalente do íris GL, exceto a chamada para **bbox2**.</span><span class="sxs-lookup"><span data-stu-id="e5ffe-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="e5ffe-111">Use o código do Windows apropriado para desenhar um retângulo com o mesmo tamanho que o íris GL **bbox**.</span><span class="sxs-lookup"><span data-stu-id="e5ffe-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 




