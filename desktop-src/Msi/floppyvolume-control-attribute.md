---
description: Se o bit de controle FloppyVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de controle FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947007"
---
# <a name="floppyvolume-control-attribute"></a>Atributo de controle FloppyVolume

Se o bit de controle FloppyVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disquete.

Se esse bit não estiver definido, o controle listará os volumes na instalação atual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit FloppyVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



