---
description: As dimensões de uma caneta superficial são especificadas em unidades de dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Canetas cosméticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65f875ce5873b5f53cba19b5440751b8ac7683df99765ea7e8e6eec813ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966066"
---
# <a name="cosmetic-pens"></a>Canetas cosméticas

As dimensões de uma caneta superficial são especificadas em unidades de dispositivo. Portanto, as linhas desenhadas com uma caneta cosmética sempre têm uma largura fixa. Linhas desenhadas com uma caneta cosmética geralmente são desenhadas 3 a 10 vezes mais rápido do que as linhas desenhadas com uma caneta geométrica. As canetas cosméticas têm três atributos: largura, estilo e cor. Para obter mais informações sobre esses atributos, consulte [Atributos de caneta.](pen-attributes.md)

Para criar uma caneta superficial, use a [**função CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Para recuperar uma das três canetas cosméticas de estoque gerenciadas pelo sistema, use a [**função GetStockObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)

Depois de criar uma caneta (ou obter um alça para uma das canetas de estoque), selecione a caneta no DC (contexto do dispositivo) do aplicativo usando a [**função SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Desse ponto em diante, o aplicativo usa essa caneta para qualquer operação de desenho de linha em sua área de cliente.

 

 



