---
description: Os primitivos que ficam parcialmente dentro (ou completamente fora) da exibição frustum podem ser recortados para que apenas a parte visível do primitivo seja renderizada.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Estado de recorte primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370333"
---
# <a name="primitive-clipping-state-direct3d-9"></a>Estado de recorte primitivo (Direct3D 9)

Os primitivos que ficam parcialmente dentro (ou completamente fora) da [exibição frustum](viewports-and-clipping.md) podem ser recortados para que apenas a parte visível do primitivo seja renderizada. O recorte reduz a quantidade de trabalho feita apenas para os primitivos ou partes de um primitivo que ficará visível.

Para usar o pipeline para recorte, defina o \_ estado de renderização de recorte D3DRS como **true** (o valor padrão) para habilitar o recorte ou **false** para desabilitar o recorte de Direct3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 



