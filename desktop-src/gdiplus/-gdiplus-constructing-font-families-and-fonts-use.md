---
description: O Windows GDI+ agrupa fontes com a mesma face de tipos, mas estilos diferentes em famílias de fontes.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construindo fontes e famílias de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988887"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="79242-103">Construindo fontes e famílias de fontes</span><span class="sxs-lookup"><span data-stu-id="79242-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="79242-104">O Windows GDI+ agrupa fontes com a mesma face de tipos, mas estilos diferentes em famílias de fontes.</span><span class="sxs-lookup"><span data-stu-id="79242-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="79242-105">Por exemplo, a família de fonte Arial contém as seguintes fontes:</span><span class="sxs-lookup"><span data-stu-id="79242-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="79242-106">Arial Regular</span><span class="sxs-lookup"><span data-stu-id="79242-106">Arial Regular</span></span>
-   <span data-ttu-id="79242-107">Arial Bold</span><span class="sxs-lookup"><span data-stu-id="79242-107">Arial Bold</span></span>
-   <span data-ttu-id="79242-108">Arial Italic</span><span class="sxs-lookup"><span data-stu-id="79242-108">Arial Italic</span></span>
-   <span data-ttu-id="79242-109">Arial Bold Italic</span><span class="sxs-lookup"><span data-stu-id="79242-109">Arial Bold Italic</span></span>

<span data-ttu-id="79242-110">O GDI+ usa quatro estilos para formar famílias: regular, negrito, itálico e negrito itálico.</span><span class="sxs-lookup"><span data-stu-id="79242-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="79242-111">Adjetivos como *estreito* e *arredondado* não são considerados estilos; em vez disso, eles são parte do nome da família.</span><span class="sxs-lookup"><span data-stu-id="79242-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="79242-112">Por exemplo, Arial Narrow é uma família de fontes cujos membros são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="79242-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="79242-113">Arial Narrow Regular</span><span class="sxs-lookup"><span data-stu-id="79242-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="79242-114">Arial Narrow Bold</span><span class="sxs-lookup"><span data-stu-id="79242-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="79242-115">Arial Narrow Italic</span><span class="sxs-lookup"><span data-stu-id="79242-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="79242-116">Arial Narrow Bold Italic</span><span class="sxs-lookup"><span data-stu-id="79242-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="79242-117">Antes de poder desenhar o texto com o GDI+, você precisa construir um objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) e um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="79242-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="79242-118">Os objetos **FontFamily** especifica a face de tipos (por exemplo, Arial) e o objeto **Font** especifica o tamanho, o estilo e as unidades.</span><span class="sxs-lookup"><span data-stu-id="79242-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="79242-119">O exemplo a seguir constrói uma fonte Arial de estilo regular com um tamanho de 16 pixels:</span><span class="sxs-lookup"><span data-stu-id="79242-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="79242-120">No código anterior, o primeiro argumento passado para o construtor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) é o endereço do objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="79242-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="79242-121">O segundo argumento especifica o tamanho da fonte medido em unidades identificadas pelo quarto argumento.</span><span class="sxs-lookup"><span data-stu-id="79242-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="79242-122">O terceiro argumento identifica o estilo.</span><span class="sxs-lookup"><span data-stu-id="79242-122">The third argument identifies the style.</span></span>

<span data-ttu-id="79242-123">\* \* \* \* [UnitPixel \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* \* é um membro da enumeração **de unidade** e [\* \* \* \* FontStyleRegular \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) é um membro da enumeração **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="79242-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="79242-124">Ambas as enumerações são declaradas em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="79242-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



