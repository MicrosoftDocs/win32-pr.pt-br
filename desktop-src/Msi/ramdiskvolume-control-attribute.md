---
description: Se esse bit estiver definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco ram. Se esse bit não estiver definido, o controle lista os volumes na instalação atual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de controle RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9167c045a8437fff12c312999d71bd8fc2c7927f1ac8d3acf2260127b73cbb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129016"
---
# <a name="ramdiskvolume-control-attribute"></a>Atributo de controle RAMDiskVolume

Se esse bit estiver definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco ram. Se esse bit não estiver definido, o controle lista os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit RAMDiskVolume na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



