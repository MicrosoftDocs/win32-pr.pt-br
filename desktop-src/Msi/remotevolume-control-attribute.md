---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes remotos. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Atributo de controle RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787071"
---
# <a name="remotevolume-control-attribute"></a>Atributo de controle RemoteVolume

Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes remotos. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit RemoteVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



