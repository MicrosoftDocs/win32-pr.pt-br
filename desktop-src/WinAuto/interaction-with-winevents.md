---
title: Interação com WinEvents
description: O tempo de execução da anotação dinâmica não enviará WinEvents; é responsabilidade do anotador enviar eventos apropriados, quando necessário. Se você precisar enviar WinEvents, não se esqueça de enviá-los depois que a anotação tiver sido feita.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "105815553"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="2f40e-104">Interação com WinEvents</span><span class="sxs-lookup"><span data-stu-id="2f40e-104">Interaction with WinEvents</span></span>

<span data-ttu-id="2f40e-105">O tempo de execução da anotação dinâmica não enviará [WinEvents](winevents-infrastructure.md); é responsabilidade do anotador enviar eventos apropriados, quando necessário.</span><span class="sxs-lookup"><span data-stu-id="2f40e-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="2f40e-106">Se você precisar enviar WinEvents, não se esqueça de enviá-los depois que a anotação tiver sido feita.</span><span class="sxs-lookup"><span data-stu-id="2f40e-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="2f40e-107">Por exemplo, se você usar [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir a propriedade [**Name**](name-property.md) de um elemento, envie um evento [**Event \_ Object \_ NAMECHANGE**](event-constants.md) para esse objeto depois que **SetPropValue** retornar.</span><span class="sxs-lookup"><span data-stu-id="2f40e-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="2f40e-108">No entanto, se você usar [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir o ValueMap para um Slider, nenhum evento será necessário porque a definição de ValueMap não altera o valor do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="2f40e-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




