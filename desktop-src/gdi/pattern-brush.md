---
description: Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo). Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pincel de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48b7d5f3bc5c4b0fd86eda28a35bb56f02e5ba998353d36d829a71655aa66f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831516"
---
# <a name="pattern-brush"></a>Pincel de padrão

Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo). Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.

![ilustração mostrando três caixas, cada uma preenchida com um padrão diferente](images/csbru-05.png)

Para criar um pincel de padrão lógico, um aplicativo deve primeiro criar um bitmap. Depois de criar o bitmap, o aplicativo pode criar o pincel de padrão lógico chamando a função [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , fornecendo um identificador que identifica o bitmap (ou DIB). Os pincéis que aparecem na ilustração anterior foram criados a partir de bitmaps monocromáticos. Para obter uma descrição de bitmaps, DIBs e as funções que os criam, consulte [bitmaps](bitmaps.md).

 

 



