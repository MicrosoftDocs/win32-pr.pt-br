---
description: Uma corda é uma região limitada pela interseção de uma elipse e um segmento de linha chamado de secante. A ilustração a seguir mostra uma corda desenhada usando a função de corda.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Sobre as cordas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502206"
---
# <a name="about-chords"></a><span data-ttu-id="e4021-104">Sobre as cordas</span><span class="sxs-lookup"><span data-stu-id="e4021-104">About Chords</span></span>

<span data-ttu-id="e4021-105">Uma *corda* é uma região limitada pela interseção de uma elipse e um segmento de linha chamado de *secante*.</span><span class="sxs-lookup"><span data-stu-id="e4021-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="e4021-106">A ilustração a seguir mostra uma corda desenhada usando a função de [**corda**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .</span><span class="sxs-lookup"><span data-stu-id="e4021-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![ilustração de um elipse, mostrando dois radials, uma secante e uma corda](images/csfsh-02.png)

<span data-ttu-id="e4021-108">Ao chamar a [**corda**](/windows/win32/api/wingdi/nf-wingdi-chord), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radials.</span><span class="sxs-lookup"><span data-stu-id="e4021-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="e4021-109">Um radial é uma linha desenhada do centro do retângulo delimitador de uma elipse para um ponto na elipse.</span><span class="sxs-lookup"><span data-stu-id="e4021-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="e4021-110">Quando o sistema desenha a parte curva da corda, ele faz isso usando a direção do arco atual para o contexto do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e4021-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="e4021-111">A direção do arco padrão é anti-horário.</span><span class="sxs-lookup"><span data-stu-id="e4021-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="e4021-112">Você pode fazer com que seu aplicativo redefina a direção do arco chamando a função [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="e4021-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
