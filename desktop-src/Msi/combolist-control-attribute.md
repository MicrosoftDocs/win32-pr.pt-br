---
description: Se o bit de controle de combinação de combinações for definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático. Isso impede que um usuário insira um novo valor e exige que o usuário escolha apenas um dos valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de controle de combinação de combinações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757526"
---
# <a name="combolist-control-attribute"></a>Atributo de controle de combinação de combinações

Se o bit de controle de combinação de combinações for definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático. Isso impede que um usuário insira um novo valor e exige que o usuário escolha apenas um dos valores predefinidos.

Se esse bit não estiver definido, a caixa de combinação terá um campo de edição.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Descrição                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit de combinação na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



