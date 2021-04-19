---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco de RAM. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de controle RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768721"
---
# <a name="ramdiskvolume-control-attribute"></a>Atributo de controle RAMDiskVolume

Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco de RAM. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit RAMDiskVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



