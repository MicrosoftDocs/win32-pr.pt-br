---
description: Primitivos que ficam parcialmente dentro (ou completamente fora) da exibição podem ser recortados para que apenas a parte visível do primitivo seja renderizada.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Estado de recorte primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864d1083d7a94283ccf097de21dfbd8c7d1320d9876ceb3d7c33b6714bd169d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092771"
---
# <a name="primitive-clipping-state-direct3d-9"></a>Estado de recorte primitivo (Direct3D 9)

Primitivos que ficam parcialmente dentro (ou completamente fora) da exibição [podem](viewports-and-clipping.md) ser recortados para que apenas a parte visível do primitivo seja renderizada. O recorte reduz a quantidade de trabalho que é feita apenas para os primitivos ou partes de um primitivo que estarão visíveis.

Para usar o pipeline para recorte, de definido o estado de renderização D3DRS CLIPPING como TRUE (o valor padrão) para habilitar o recorte ou como FALSE para desabilitar o \_ recorte direct3D.  

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar estados](render-states.md)
</dt> </dl>

 

 



