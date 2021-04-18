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
# <a name="interaction-with-winevents"></a>Interação com WinEvents

O tempo de execução da anotação dinâmica não enviará [WinEvents](winevents-infrastructure.md); é responsabilidade do anotador enviar eventos apropriados, quando necessário. Se você precisar enviar WinEvents, não se esqueça de enviá-los depois que a anotação tiver sido feita.

Por exemplo, se você usar [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir a propriedade [**Name**](name-property.md) de um elemento, envie um evento [**Event \_ Object \_ NAMECHANGE**](event-constants.md) para esse objeto depois que **SetPropValue** retornar.

No entanto, se você usar [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir o ValueMap para um Slider, nenhum evento será necessário porque a definição de ValueMap não altera o valor do controle deslizante.

 

 




