---
description: Se esse bit for definido, a caixa de diálogo chamará periodicamente o instalador.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit de estilo de caixa de diálogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810566"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Bit de estilo de caixa de diálogo TrackDiskSpace

Se esse bit for definido, a caixa de diálogo chamará periodicamente o instalador. Se a propriedade for alterada, ela notificará os controles na caixa de diálogo. Esse estilo pode ser usado se houver um controle na caixa de diálogo que indique espaço em disco. Se o usuário alternar para outro aplicativo, adicionar ou remover arquivos ou, de outra forma, modificar o espaço em disco disponível, você poderá implementar rapidamente a alteração usando esse estilo.

Qualquer caixa de diálogo que dependa da propriedade [**OutOfDiskSpace**](outofdiskspace.md) para determinar se um diálogo deve ser definido por um bit de estilo de caixa de diálogo TrackDiskSpace para a caixa de diálogo para atualizar dinamicamente o espaço nos volumes de destino.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



