---
description: Uma pizza é uma região limitada pela interseção de uma curva de elipse e duas radials. A ilustração a seguir mostra uma pizza desenhada usando a função de pizza.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Sobre as tortas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010742"
---
# <a name="about-pies"></a><span data-ttu-id="86478-104">Sobre as tortas</span><span class="sxs-lookup"><span data-stu-id="86478-104">About Pies</span></span>

<span data-ttu-id="86478-105">Uma *pizza* é uma região limitada pela interseção de uma curva de elipse e duas radials.</span><span class="sxs-lookup"><span data-stu-id="86478-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="86478-106">A ilustração a seguir mostra uma pizza desenhada usando a função de [**pizza**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .</span><span class="sxs-lookup"><span data-stu-id="86478-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![ilustração mostrando uma elipse com uma pizza sombreada](images/csfsh-03.png)

<span data-ttu-id="86478-108">Ao chamar a [**pizza**](/windows/win32/api/wingdi/nf-wingdi-pie), um aplicativo fornece as coordenadas dos cantos superior esquerdo e inferior direito do retângulo delimitador da elipse, bem como as coordenadas de dois pontos que definem dois radials.</span><span class="sxs-lookup"><span data-stu-id="86478-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="86478-109">Quando o sistema desenha a parte curva da pizza, ele usa a direção do arco atual para o contexto do dispositivo fornecido.</span><span class="sxs-lookup"><span data-stu-id="86478-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="86478-110">A direção do arco padrão é anti-horário.</span><span class="sxs-lookup"><span data-stu-id="86478-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="86478-111">Um aplicativo pode redefinir a direção do arco chamando a função [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="86478-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
