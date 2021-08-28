---
description: Se o bit de controle FixedSize for definido, a imagem será cortada ou centralizada no controle sem alterar sua forma ou tamanho.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de controle FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649696"
---
# <a name="fixedsize-control-attribute"></a>Atributo de controle FixedSize

Se o bit de controle FixedSize for definido, a imagem será cortada ou centralizada no controle sem alterar sua forma ou tamanho.

Se esse bit não estiver definido, a imagem será ampliada para se ajustar ao controle.

## <a name="valid-controls"></a>Controles válidos

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Ícone](icon-control.md)

[Botão](pushbutton-control.md)

[Botão de opção](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit FixedSize na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Definir o bit FixedSize não terá nenhum efeito em [uma caixa de seleção](checkbox-control.md), um botão de [pressão](pushbutton-control.md)ou um grupo de [botões](radiobuttongroup-control.md) , se nem o [bitmap](bitmap-control-attribute.md) ou o [ícone](icon-control-attribute.md) tiverem sido definidos.

Definir o bit FixedSize não terá nenhum efeito sobre um controle de ícone ou uma pressão associada a um ícone se os bits de [ícones](iconsize-control-attribute.md) não estiverem definidos.

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



