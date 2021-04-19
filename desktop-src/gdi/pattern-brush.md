---
description: Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo). Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pincel de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988319"
---
# <a name="pattern-brush"></a>Pincel de padrão

Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo). Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.

![ilustração mostrando três caixas, cada uma preenchida com um padrão diferente](images/csbru-05.png)

Para criar um pincel de padrão lógico, um aplicativo deve primeiro criar um bitmap. Depois de criar o bitmap, o aplicativo pode criar o pincel de padrão lógico chamando a função [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , fornecendo um identificador que identifica o bitmap (ou DIB). Os pincéis que aparecem na ilustração anterior foram criados a partir de bitmaps monocromáticos. Para obter uma descrição de bitmaps, DIBs e as funções que os criam, consulte [bitmaps](bitmaps.md).

 

 



