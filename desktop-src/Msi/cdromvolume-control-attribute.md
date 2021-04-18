---
description: Se o bit de controle CDROMVolume for definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Atributo de controle CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749593"
---
# <a name="cdromvolume-control-attribute"></a>Atributo de controle CDROMVolume

Se o bit de controle CDROMVolume for definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.

Se esse bit não estiver definido, o controle mostrará todos os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit CDROMVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



