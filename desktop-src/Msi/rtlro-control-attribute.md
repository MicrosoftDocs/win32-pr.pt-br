---
description: Se esse bit de estilo for definido, o texto no controle será exibido em uma ordem de leitura da direita para a esquerda.
ms.assetid: 68394498-98ca-4bcd-86c0-3f692a26a258
title: Atributo de controle RTLRO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c4488b31b0bac714d0f28915c074c0a6e4a8b5105e3ef2be60f3870ebcf88d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039666"
---
# <a name="rtlro-control-attribute"></a>Atributo de controle RTLRO

Se esse bit de estilo for definido, o texto no controle será exibido em uma ordem de leitura da direita para a esquerda.

## <a name="valid-controls"></a>Controles válidos

[GroupBox](groupbox-control.md)

 

[ProgressBar](progressbar-control.md)

 

[Botão](pushbutton-control.md)

 

[ScrollableText](scrollabletext-control.md)

 

[Text](text-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[CheckBox](checkbox-control.md)

 

[ComboBox](combobox-control.md)

 

[Directorylist](directorylist-control.md)

 

[DirectoryCombo](directorycombo-control.md)

 

[Editar](edit-control.md)

 

[PathEdit](pathedit-control.md)

 

[ListBox](listbox-control.md)

 

[ListView](listview-control.md)

 

[Botão de opção](radiobuttongroup-control.md)

 

[SelectionTree](selectiontree-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                        |
|---------|-------------|---------------------------------|
| 32      | 0x00000020  | **msidbControlAttributesRTLRO** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit RTLRO na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



