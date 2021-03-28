---
description: Um objeto gráfico fornece métodos como DrawLine, DrawImage e DrawString para exibir imagens vetoriais, imagens rasterizadas e texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Usando contêineres de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967739"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="d99da-103">Usando contêineres de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="d99da-103">Using Graphics Containers</span></span>

<span data-ttu-id="d99da-104">Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece métodos como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para exibir imagens vetoriais, imagens rasterizadas e texto.</span><span class="sxs-lookup"><span data-stu-id="d99da-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="d99da-105">Um objeto **gráfico** também tem várias propriedades que influenciam a qualidade e a orientação dos itens que são desenhados.</span><span class="sxs-lookup"><span data-stu-id="d99da-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="d99da-106">Por exemplo, a propriedade de modo de suavização determina se a suavização é aplicada às linhas e curvas e a propriedade de transformação global influencia a posição e a rotação dos itens que são desenhados.</span><span class="sxs-lookup"><span data-stu-id="d99da-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="d99da-107">Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) geralmente é associado a um dispositivo de vídeo específico.</span><span class="sxs-lookup"><span data-stu-id="d99da-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="d99da-108">Quando você usa um objeto **Graphics** para desenhar em uma janela, o objeto **Graphics** também é associado a essa janela específica.</span><span class="sxs-lookup"><span data-stu-id="d99da-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="d99da-109">Um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pode ser considerado um contêiner porque contém um conjunto de propriedades que influenciam o desenho e é vinculado a informações específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d99da-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="d99da-110">Você pode criar um contêiner secundário dentro de um objeto **gráfico** existente chamando o método [BeginContainer](/previous-versions//ms535731(v=vs.85)) do objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d99da-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="d99da-111">Os tópicos a seguir abordam objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e contêineres aninhados com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="d99da-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="d99da-112">O estado de um objeto de elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="d99da-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="d99da-113">Contêineres de elementos gráficos aninhados</span><span class="sxs-lookup"><span data-stu-id="d99da-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
