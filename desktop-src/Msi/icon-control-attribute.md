---
description: Se esse bit for definido, o texto será substituído por uma imagem de ícone e a coluna de texto na tabela de controle será uma chave estrangeira na tabela binária.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Atributo de controle de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2caeb407b86b888a5dd3b1c08f16d0893233f82cec29b92519c267b286ea121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315116"
---
# <a name="icon-control-attribute"></a>Atributo de controle de ícone

Se esse bit for definido, o texto será substituído por uma imagem de ícone e a coluna de texto na [tabela de controle](control-table.md) será uma chave estrangeira na [tabela binária](binary-table.md).

Se esse bit não estiver definido, o texto no controle será especificado na coluna de texto da [tabela de controle](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Botão](pushbutton-control.md)

[Botão de opção](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua os bits do ícone na coluna atributos do registro do controle na tabela de [controle](control-table.md).

A coluna de texto na tabela de controle é usada como uma chave estrangeira para a [tabela binária](binary-table.md), portanto, o controle não pode conter uma imagem de ícone e um texto.

Não defina os bits de ícone e [bitmap](bitmap-control-attribute.md) .

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



