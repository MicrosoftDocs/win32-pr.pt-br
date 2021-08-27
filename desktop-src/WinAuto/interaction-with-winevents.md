---
title: Interação com WinEvents
description: O tempo de run time de Anotação Dinâmica não enviará WinEvents; É responsabilidade do anotador enviar eventos apropriados, quando necessário. Se você precisar enviar WinEvents, certifique-se de enviá-los depois que a anotação tiver sido realizada.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098456"
---
# <a name="interaction-with-winevents"></a>Interação com WinEvents

O tempo de run time de Anotação Dinâmica não enviará [WinEvents](winevents-infrastructure.md); É responsabilidade do anotador enviar eventos apropriados, quando necessário. Se você precisar enviar WinEvents, certifique-se de enviá-los depois que a anotação tiver sido realizada.

Por exemplo, se você usar [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir a propriedade [**Name**](name-property.md) de um elemento, envie um evento [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) para esse objeto depois que **SetPropValue** retornar.

No entanto, se você usar [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para definir o ValueMap para um controle deslizante, nenhum evento será necessário porque a configuração do ValueMap não altera o valor do controle deslizante.

 

 




