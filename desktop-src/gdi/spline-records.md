---
description: Os registros de spline representam as curvas quadráticas (isto é, linha de b quadrática) usadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Registros de spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661966"
---
# <a name="spline-records"></a><span data-ttu-id="b00f0-103">Registros de spline</span><span class="sxs-lookup"><span data-stu-id="b00f0-103">Spline Records</span></span>

<span data-ttu-id="b00f0-104">Os registros de spline representam as curvas quadráticas (isto é, linha de b quadrática) usadas por TrueType.</span><span class="sxs-lookup"><span data-stu-id="b00f0-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="b00f0-105">Um registro de spline começa com o último ponto no registro anterior (ou para o primeiro registro na delimitação, com o ponto de partida).</span><span class="sxs-lookup"><span data-stu-id="b00f0-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="b00f0-106">Para o primeiro registro spline, o ponto inicial e o último ponto no registro estão no contorno de glifo.</span><span class="sxs-lookup"><span data-stu-id="b00f0-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="b00f0-107">Para todos os outros registros de spline, apenas o último ponto está no contorno de glifo.</span><span class="sxs-lookup"><span data-stu-id="b00f0-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="b00f0-108">Todos os outros pontos nos registros de spline estão fora do contorno de glifo e devem ser renderizados como os pontos de controle de linhas b.</span><span class="sxs-lookup"><span data-stu-id="b00f0-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="b00f0-109">O último registro de spline ou polilinha em uma delimitação sempre termina com o ponto inicial da delimitação.</span><span class="sxs-lookup"><span data-stu-id="b00f0-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="b00f0-110">Essa organização garante que cada contorno seja fechado.</span><span class="sxs-lookup"><span data-stu-id="b00f0-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="b00f0-111">Como as splines b exigem três pontos (um ponto fora do contorno de glifo entre dois pontos que estão na estrutura de tópicos), você deve executar alguns cálculos quando um registro spline contiver mais de um ponto fora da curva.</span><span class="sxs-lookup"><span data-stu-id="b00f0-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="b00f0-112">Por exemplo, se um registro de spline contiver três pontos (A, B e C) e não for o primeiro registro, os pontos A e B estarão fora do contorno de glifo.</span><span class="sxs-lookup"><span data-stu-id="b00f0-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="b00f0-113">Para interpretar o ponto A, use a posição atual (que sempre está no contorno do glifo) e o ponto na estrutura de tópicos do glifo entre os pontos A e B. Para localizar o ponto médio (M) entre A e B, você pode executar o cálculo a seguir.</span><span class="sxs-lookup"><span data-stu-id="b00f0-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="b00f0-114">M = A + (B A)/2</span><span class="sxs-lookup"><span data-stu-id="b00f0-114">M = A + (B A)/2</span></span>

<span data-ttu-id="b00f0-115">O ponto médio entre os pontos fora da estrutura de tópicos consecutivos em um registro spline é um ponto no contorno do glifo, de acordo com a definição do formato spline usado em fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="b00f0-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="b00f0-116">Se a posição atual for designada por P, as duas splines quadráticas definidas por esse registro spline serão (P, A, M) e (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="b00f0-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



