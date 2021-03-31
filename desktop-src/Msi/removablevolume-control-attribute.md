---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes removíveis. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Atributo de controle RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647056"
---
# <a name="removablevolume-control-attribute"></a>Atributo de controle RemovableVolume

Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes removíveis. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit RemovableVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



