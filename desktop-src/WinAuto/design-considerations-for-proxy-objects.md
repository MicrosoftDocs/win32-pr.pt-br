---
title: Considerações de design para objetos de proxy
description: O design de objeto de proxy e acessível depende do design dos elementos de interface do usuário do servidor. Independentemente do design, um elemento de interface do usuário deve notificar seu objeto proxy logo antes que ele seja destruído para que o objeto proxy manipule chamadas de clientes adequadamente.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005106"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="94b22-104">Considerações de design para objetos de proxy</span><span class="sxs-lookup"><span data-stu-id="94b22-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="94b22-105">O design de objeto de proxy e acessível depende do design dos elementos de interface do usuário do servidor.</span><span class="sxs-lookup"><span data-stu-id="94b22-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="94b22-106">Independentemente do design, um elemento de interface do usuário deve notificar seu objeto proxy logo antes que ele seja destruído para que o objeto proxy manipule chamadas de clientes adequadamente.</span><span class="sxs-lookup"><span data-stu-id="94b22-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="94b22-107">A lista a seguir descreve duas possibilidades de design:</span><span class="sxs-lookup"><span data-stu-id="94b22-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="94b22-108">Coloque o código que implementa a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no mesmo módulo que o código que implementa o elemento de interface do usuário se o código da interface do usuário for facilmente extensível.</span><span class="sxs-lookup"><span data-stu-id="94b22-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="94b22-109">Nesse caso, o proxy é "leve" no sentido de que tudo o que ele faz é monitorar o período de vida do objeto acessível, encaminhar chamadas para o objeto acessível e retornar os resultados.</span><span class="sxs-lookup"><span data-stu-id="94b22-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="94b22-110">Coloque o código que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no mesmo módulo que o código que implementa o objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="94b22-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="94b22-111">Nesse caso, o objeto acessível usa funções internas para obter informações sobre o elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="94b22-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="94b22-112">Controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="94b22-112">Trackbar Controls</span></span>

<span data-ttu-id="94b22-113">Ao implementar controles TrackBar, use o estilo TrackBar **TBS \_ invertido** para fornecer informações mais significativas.</span><span class="sxs-lookup"><span data-stu-id="94b22-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="94b22-114">Esse estilo inverte a escala usada por [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="94b22-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="94b22-115">Para trackbars verticais sem esse estilo, [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retorna zero (0) quando o TrackBar Thumb está na parte superior do controle; os valores aumentam à medida que você desliza o polegar para a parte inferior.</span><span class="sxs-lookup"><span data-stu-id="94b22-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="94b22-116">Com o **estilo \_ revertido TBS** , **IAccessible:: get \_ accValue** retorna 100 (100) quando o TrackBar Thumb está na parte superior; os números diminuem à medida que você move o TrackBar Thumb para a parte inferior.</span><span class="sxs-lookup"><span data-stu-id="94b22-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="94b22-117">Para trackbars horizontais sem esse estilo, zero (0) é retornado quando o TrackBar Thumb está na extremidade esquerda do controle; os valores aumentam à medida que você move o TrackBar Thumb para a direita.</span><span class="sxs-lookup"><span data-stu-id="94b22-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="94b22-118">Com o **estilo \_ revertido TBS** , [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retorna 100 (100) quando o TrackBar Thumb está à esquerda; os valores diminuem à medida que você move o TrackBar Thumb para a direita.</span><span class="sxs-lookup"><span data-stu-id="94b22-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




