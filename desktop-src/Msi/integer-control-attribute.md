---
description: Se esse bit for definido em um controle, a propriedade associada especificada na coluna propriedade da tabela de controle será um número inteiro. Se esse bit não for definido, a propriedade será um valor de cadeia de caracteres.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Atributo de controle de inteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812917"
---
# <a name="integer-control-attribute"></a>Atributo de controle de inteiro

Se esse bit for definido em um controle, a propriedade associada especificada na coluna propriedade da tabela de [controle](control-table.md) será um número inteiro. Se esse bit não for definido, a propriedade será um valor de cadeia de caracteres.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[ComboBox](combobox-control.md)

[Editar](edit-control.md)

[ListBox](listbox-control.md)

[Botão de opção](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 16      | 0x00000010  | **msidbControlAttributesInteger** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit inteiro na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



