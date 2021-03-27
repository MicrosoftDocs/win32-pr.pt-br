---
description: As dimensões de uma caneta superficial são especificadas em unidades do dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Canetas superficiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661623"
---
# <a name="cosmetic-pens"></a>Canetas superficiais

As dimensões de uma caneta superficial são especificadas em unidades do dispositivo. Portanto, as linhas desenhadas com uma caneta superficial sempre têm uma largura fixa. As linhas desenhadas com uma caneta superficial geralmente são desenhadas de 3 a 10 vezes mais rápido do que as linhas desenhadas com uma caneta geométrica. As canetas superficiais têm três atributos: largura, estilo e cor. Para obter mais informações sobre esses atributos, consulte [atributos de caneta](pen-attributes.md).

Para criar uma caneta superficial, use a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Para recuperar uma das três canetas de superficial de estoque gerenciadas pelo sistema, use a função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .

Depois de criar uma caneta (ou obter um identificador para uma das canetas de ações), selecione a caneta no contexto do dispositivo do aplicativo (DC) usando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . A partir desse ponto, o aplicativo usa essa caneta para qualquer operação de desenho de linha em sua área de cliente.

 

 



