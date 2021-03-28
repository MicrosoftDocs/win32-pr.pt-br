---
description: Um polígono é uma forma preenchida com lados retos.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Sobre polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010741"
---
# <a name="about-polygons"></a><span data-ttu-id="323c4-103">Sobre polígonos</span><span class="sxs-lookup"><span data-stu-id="323c4-103">About Polygons</span></span>

<span data-ttu-id="323c4-104">Um *polígono* é uma forma preenchida com lados retos.</span><span class="sxs-lookup"><span data-stu-id="323c4-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="323c4-105">Os lados de um polígono são desenhados usando a caneta atual.</span><span class="sxs-lookup"><span data-stu-id="323c4-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="323c4-106">Quando o sistema preenche um polígono, ele usa o pincel atual e o modo de preenchimento do polígono atual.</span><span class="sxs-lookup"><span data-stu-id="323c4-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="323c4-107">Os dois modos de preenchimento, alternativo (o padrão) e o enrolamento, determinam se as regiões em um polígono complexo são preenchidas ou deixadas como não pintadas.</span><span class="sxs-lookup"><span data-stu-id="323c4-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="323c4-108">Um aplicativo pode selecionar um dos modos chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="323c4-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="323c4-109">Para obter mais informações sobre os modos de preenchimento de polígono, consulte [regiões](regions.md).</span><span class="sxs-lookup"><span data-stu-id="323c4-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="323c4-110">A ilustração a seguir mostra um polígono desenhado usando o [**polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span><span class="sxs-lookup"><span data-stu-id="323c4-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![ilustração de um polígono na forma de uma estrela de cinco pontas](images/csfsh-04.png)

<span data-ttu-id="323c4-112">Além de desenhar um único polígono usando [**polígono**](/windows/win32/api/wingdi/nf-wingdi-polygon), um aplicativo pode desenhar vários polígonos usando a função [**polipolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .</span><span class="sxs-lookup"><span data-stu-id="323c4-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
