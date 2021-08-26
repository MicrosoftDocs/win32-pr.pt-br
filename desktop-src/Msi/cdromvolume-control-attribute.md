---
description: Se o bit controle CDROMVolume estiver definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Atributo de controle CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078036"
---
# <a name="cdromvolume-control-attribute"></a>Atributo de controle CDROMVolume

Se o bit controle CDROMVolume estiver definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.

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

Para definir esse atributo em um controle, inclua o bit CDROMVolume na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Atributos de controle](control-attributes.md) e o controle que você precisa criar em [Controles](controls.md).

 

 



