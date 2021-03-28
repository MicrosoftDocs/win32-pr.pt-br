---
description: Este tópico lista os construtores da classe Region. Para obter uma listagem de classe completa, consulte região classe.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Construtores Region. Region
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091479"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="87632-104">Construtores Region. Region</span><span class="sxs-lookup"><span data-stu-id="87632-104">Region.Region constructors</span></span>

<span data-ttu-id="87632-105">Este tópico lista os construtores da classe [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) .</span><span class="sxs-lookup"><span data-stu-id="87632-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="87632-106">Para obter uma listagem de classe completa, consulte **região classe**.</span><span class="sxs-lookup"><span data-stu-id="87632-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="87632-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="87632-107">Overload list</span></span>



| <span data-ttu-id="87632-108">Construtor</span><span class="sxs-lookup"><span data-stu-id="87632-108">Constructor</span></span>                                                                 | <span data-ttu-id="87632-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="87632-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87632-110">[**Região (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="87632-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="87632-111">Cria uma região que é idêntica à região especificada por um identificador para uma região GDI.</span><span class="sxs-lookup"><span data-stu-id="87632-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="87632-112">[**Região (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="87632-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="87632-113">Cria uma região que é definida por um retângulo.</span><span class="sxs-lookup"><span data-stu-id="87632-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="87632-114">[**Região (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="87632-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="87632-115">Cria uma região que é definida por um retângulo.</span><span class="sxs-lookup"><span data-stu-id="87632-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="87632-116">[**Região (BYTE \* , int)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="87632-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="87632-117">Cria uma região que é definida por dados obtidos de outra região.</span><span class="sxs-lookup"><span data-stu-id="87632-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="87632-118">[**Região (GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="87632-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="87632-119">Cria uma região que é definida por um caminho (um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ) e tem um modo de preenchimento que está contido no objeto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="87632-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="87632-120">[**Região ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="87632-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="87632-121">Cria uma região infinita.</span><span class="sxs-lookup"><span data-stu-id="87632-121">Creates a region that is infinite.</span></span> <span data-ttu-id="87632-122">Esse é o construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="87632-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
