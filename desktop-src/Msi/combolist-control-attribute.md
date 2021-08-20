---
description: Se o bit Controle ComboList estiver definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático. Isso impede que um usuário entre um novo valor e exija que o usuário escolha apenas um dos valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de controle ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e0a53357d91c5c5a016f65e8e1e0fb341b15cae1ea2c6cf480e536fa109067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145375"
---
# <a name="combolist-control-attribute"></a>Atributo de controle ComboList

Se o bit Controle ComboList estiver definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático. Isso impede que um usuário entre um novo valor e exija que o usuário escolha apenas um dos valores predefinidos.

Se esse bit não estiver definido, a caixa de combinação terá um campo de edição.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Descrição                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit ComboList na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Atributos de controle](control-attributes.md) e o controle que você precisa criar em [Controles](controls.md).

 

 



