---
description: O Windows GDI+ fornece várias classes que formam a base para o desenho de texto.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Usando texto e fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501657"
---
# <a name="using-text-and-fonts"></a><span data-ttu-id="09ee8-103">Usando texto e fontes</span><span class="sxs-lookup"><span data-stu-id="09ee8-103">Using Text and Fonts</span></span>

<span data-ttu-id="09ee8-104">O Windows GDI+ fornece várias classes que formam a base para o desenho de texto.</span><span class="sxs-lookup"><span data-stu-id="09ee8-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="09ee8-105">A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem vários métodos [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) que permitem especificar vários recursos de texto, como local, retângulo delimitador, fonte e formato.</span><span class="sxs-lookup"><span data-stu-id="09ee8-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="09ee8-106">Outras classes que contribuem para a renderização de texto incluem [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="09ee8-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="09ee8-107">Os tópicos a seguir abordam texto e fontes com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="09ee8-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="09ee8-108">Construindo fontes e famílias de fontes</span><span class="sxs-lookup"><span data-stu-id="09ee8-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="09ee8-109">Texto de desenho</span><span class="sxs-lookup"><span data-stu-id="09ee8-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="09ee8-110">Formatando texto</span><span class="sxs-lookup"><span data-stu-id="09ee8-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="09ee8-111">Enumeração de fontes instaladas</span><span class="sxs-lookup"><span data-stu-id="09ee8-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="09ee8-112">Criar uma coleções de fontes privadas</span><span class="sxs-lookup"><span data-stu-id="09ee8-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="09ee8-113">Obtendo métricas de fonte</span><span class="sxs-lookup"><span data-stu-id="09ee8-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="09ee8-114">Anti-aliasing com texto</span><span class="sxs-lookup"><span data-stu-id="09ee8-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



