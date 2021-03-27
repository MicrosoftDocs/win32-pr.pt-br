---
description: Um aplicativo cria uma região chamando uma função associada a uma forma específica. A tabela a seguir mostra as funções associadas a cada uma das formas padrão.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Criação e seleção de região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967600"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="c4678-104">Criação e seleção de região</span><span class="sxs-lookup"><span data-stu-id="c4678-104">Region Creation and Selection</span></span>

<span data-ttu-id="c4678-105">Um aplicativo cria uma região chamando uma função associada a uma forma específica.</span><span class="sxs-lookup"><span data-stu-id="c4678-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="c4678-106">A tabela a seguir mostra as funções associadas a cada uma das formas padrão.</span><span class="sxs-lookup"><span data-stu-id="c4678-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="c4678-107">Forma</span><span class="sxs-lookup"><span data-stu-id="c4678-107">Shape</span></span>                                   | <span data-ttu-id="c4678-108">Função</span><span class="sxs-lookup"><span data-stu-id="c4678-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4678-109">Região retangular</span><span class="sxs-lookup"><span data-stu-id="c4678-109">Rectangular region</span></span>                      | <span data-ttu-id="c4678-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="c4678-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="c4678-111">Região retangular com cantos arredondados</span><span class="sxs-lookup"><span data-stu-id="c4678-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="c4678-112">**CreateRoundRectRgn**</span><span class="sxs-lookup"><span data-stu-id="c4678-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="c4678-113">Região elíptica</span><span class="sxs-lookup"><span data-stu-id="c4678-113">Elliptical region</span></span>                       | <span data-ttu-id="c4678-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="c4678-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="c4678-115">Região poligonal</span><span class="sxs-lookup"><span data-stu-id="c4678-115">Polygonal region</span></span>                        | <span data-ttu-id="c4678-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="c4678-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="c4678-117">Cada função de criação de região retorna um identificador que identifica a nova região.</span><span class="sxs-lookup"><span data-stu-id="c4678-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="c4678-118">Um aplicativo pode usar esse identificador para selecionar a região em um contexto de dispositivo chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) e fornecendo esse identificador como o segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="c4678-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="c4678-119">Depois que uma região é selecionada em um contexto de dispositivo, o aplicativo pode executar várias operações nela.</span><span class="sxs-lookup"><span data-stu-id="c4678-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



