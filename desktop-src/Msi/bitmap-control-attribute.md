---
description: Se o bit de Controle de Bitmap estiver definido, o texto no controle será substituído por uma imagem de bitmap. A coluna Texto na tabela Controle é uma chave estrangeira na tabela Binária.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Atributo de controle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cd7ea8186d1ed16de71ae9974bb67a082142ed3e921d023ad905d4f47bbc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638735"
---
# <a name="bitmap-control-attribute"></a>Atributo de controle bitmap

Se o bit de Controle de Bitmap estiver definido, o texto no controle será substituído por uma imagem de bitmap. A coluna Texto na tabela [Controle é](control-table.md) uma chave estrangeira na [tabela Binária](binary-table.md).

Se esse bit não estiver definido, o texto no controle será especificado na coluna Texto da [tabela Controle](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

 

[Botão](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit Bitmap na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

A coluna Texto na tabela Controle é usada como uma chave estrangeira para a tabela [Binária,](binary-table.md)portanto, o controle não pode conter uma imagem de ícone e texto.

Não de definir os bits [Ícone](icon-control-attribute.md) e Bitmap.

Consulte [Atributos de controle](control-attributes.md) e o controle que você precisa criar em [Controles](controls.md).

 

 



