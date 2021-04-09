---
description: Se esse bit for definido, os itens listados no controle serão exibidos em uma ordem especificada. Se o bit não estiver definido, os itens serão exibidos em ordem alfabética.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Atributo de controle classificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010372"
---
# <a name="sorted-control-attribute"></a>Atributo de controle classificado

Se esse bit for definido, os itens listados no controle serão exibidos em uma ordem especificada. Se o bit não estiver definido, os itens serão exibidos em ordem alfabética.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[Controle ListView](listview-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesSorted** |



 

## <a name="remarks"></a>Comentários

Para classificar os itens em uma [ComboBox](combobox-control.md), inclua o bit classificado na coluna atributos da tabela de [controle](control-table.md) e especifique a ordem do item na coluna ordem da [tabela ComboBox](combobox-table.md).

Para classificar os itens em uma caixa de [listagem](listbox-control.md), inclua o bit classificado na coluna atributos da [tabela de controle](control-table.md) e especifique a ordem do item na coluna ordem da [tabela ComboBox](combobox-table.md).

Para classificar os itens em um [ListView](listview-control.md), inclua o bit classificado na coluna atributos da tabela de [controle](control-table.md) e especifique a ordem dos itens na [tabela ComboBox](combobox-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



