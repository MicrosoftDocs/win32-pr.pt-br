---
description: Se esse bit for definido, a barra de rolagem estará localizada no lado esquerdo do controle.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Atributo de controle LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99505e66f6f49b0a148b80a96d68bbef70d0f2b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757390"
---
# <a name="leftscroll-control-attribute"></a>Atributo de controle LeftScroll

Se esse bit for definido, a barra de rolagem estará localizada no lado esquerdo do controle.

Se esse bit não estiver definido, a barra de rolagem estará no lado direito do controle.

## <a name="valid-controls"></a>Controles válidos

[ScrollableText](scrollabletext-control.md)

[VolumeCostList](volumecostlist-control.md)

[ComboBox](combobox-control.md)

[Directorylist](directorylist-control.md)

[DirectoryCombo](directorycombo-control.md)

[Editar](edit-control.md)

[ListBox](listbox-control.md)

[ListView](listview-control.md)

[SelectionTree](selectiontree-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                             |
|---------|-------------|--------------------------------------|
| 128     | 0x00000080  | **msidbControlAttributesLeftScroll** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit LeftScroll na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



