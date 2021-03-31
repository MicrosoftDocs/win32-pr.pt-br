---
description: Se o bit de controle FixedVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os discos rígidos internos fixos.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de controle FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827605"
---
# <a name="fixedvolume-control-attribute"></a>Atributo de controle FixedVolume

Se o bit de controle FixedVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os discos rígidos internos fixos.

Se esse bit não estiver definido, o controle listará os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | Hexadecimal | Constante                              |
|---------|-------------|---------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit FixedVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



