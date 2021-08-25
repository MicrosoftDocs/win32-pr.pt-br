---
description: Várias funções usam o pincel atualmente selecionado em um contexto de dispositivo para executar operações de bitmap.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps como pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8e218180ab646de1c9c8ff622be1bcc268df73f6f4bb0b6df82482c9a2c851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944246"
---
# <a name="bitmaps-as-brushes"></a>Bitmaps como pincéis

Várias funções usam o pincel atualmente selecionado em um contexto de dispositivo para executar operações de bitmap. Por exemplo, a função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) Replica o pincel em uma região retangular dentro de uma janela, e a função [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) Replica o pincel dentro de uma área em uma janela limitada pela cor especificada (ao contrário de **PatBlt**, **FloodFill** faz o preenchimento de formas não retangulares).

A função [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) Replica o pincel dentro de uma região limitada por uma cor especificada. No entanto, ao contrário da função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , o **FloodFill** não combina os dados de cor para o pincel com os dados de cor dos pixels na exibição; Ele simplesmente define a cor de todos os pixels dentro da região incluída na exibição para a cor do pincel selecionado no momento no contexto do dispositivo.

 

 



