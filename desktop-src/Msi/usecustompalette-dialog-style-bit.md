---
description: Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado). Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit de estilo de caixa de diálogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9863f9b20ad85caf3712c3cfa00fd88de72f82b947a329d367d06f02ba06163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809476"
---
# <a name="usecustompalette-dialog-style-bit"></a>Bit de estilo de caixa de diálogo UseCustomPalette

Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado). Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.

Normalmente, um definiria esse bit se a caixa de diálogo contivesse uma imagem com uma paleta especial ou várias imagens compartilhando uma paleta personalizada. O bit não deve ser definido se a caixa de diálogo contiver várias imagens com paletas diferentes. Nesse caso, a paleta padrão provavelmente dará um resultado satisfatório para todas as imagens.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



