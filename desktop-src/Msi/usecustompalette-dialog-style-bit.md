---
description: Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado). Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit de estilo de caixa de diálogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751833"
---
# <a name="usecustompalette-dialog-style-bit"></a>Bit de estilo de caixa de diálogo UseCustomPalette

Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado). Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.

Normalmente, ele definiria esse bit se a caixa de diálogo contiver uma imagem com uma paleta especial ou várias imagens compartilhando uma paleta personalizada. O bit não deverá ser definido se a caixa de diálogo contiver várias imagens com paletas diferentes. Nesse caso, a paleta padrão tem mais probabilidade de fornecer um resultado satisfatório para todas as imagens.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



