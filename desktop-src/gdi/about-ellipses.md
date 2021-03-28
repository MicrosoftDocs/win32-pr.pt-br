---
description: Uma elipse é uma curva fechada definida por dois pontos fixos (F1 e F2), de modo que a soma das distâncias (D1 + D2) de qualquer ponto na curva até os dois pontos fixos seja constante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Sobre reticências
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550945"
---
# <a name="about-ellipses"></a><span data-ttu-id="59103-103">Sobre reticências</span><span class="sxs-lookup"><span data-stu-id="59103-103">About Ellipses</span></span>

<span data-ttu-id="59103-104">Uma elipse é uma curva fechada definida por dois pontos fixos (F1 e F2), de modo que a soma das distâncias (D1 + D2) de qualquer ponto na curva até os dois pontos fixos seja constante.</span><span class="sxs-lookup"><span data-stu-id="59103-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="59103-105">A ilustração a seguir mostra uma elipse desenhada usando a função [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .</span><span class="sxs-lookup"><span data-stu-id="59103-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![ilustração mostrando uma elipse, dois pontos fixos, duas distâncias e um retângulo delimitador](images/csfsh-01.png)

<span data-ttu-id="59103-107">Ao chamar [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse.</span><span class="sxs-lookup"><span data-stu-id="59103-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="59103-108">Um *retângulo delimitador* é o menor retângulo ao redor da elipse.</span><span class="sxs-lookup"><span data-stu-id="59103-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="59103-109">Quando o sistema desenha a elipse, ele exclui os lados direito e inferior se nenhuma transformação mundial for definida.</span><span class="sxs-lookup"><span data-stu-id="59103-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="59103-110">Portanto, para qualquer retângulo medindo x unidades de largura por unidades y alta, a elipse associada mede as unidades X1 de largura por Y1 unidades de altura.</span><span class="sxs-lookup"><span data-stu-id="59103-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="59103-111">Se o aplicativo definir uma transformação do mundo chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , o sistema incluirá os lados direito e inferior.</span><span class="sxs-lookup"><span data-stu-id="59103-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



