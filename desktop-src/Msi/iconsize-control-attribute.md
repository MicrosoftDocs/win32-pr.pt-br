---
description: Um arquivo de ícone pode conter vários tamanhos diferentes da mesma imagem de ícone.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Atributo de controle de ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7323d9c3d8dc9bef1bfd4cd275a20dfcadaa3be946bc78fd358a2d6484db53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894196"
---
# <a name="iconsize-control-attribute"></a>Atributo de controle de ícones

Um arquivo de ícone pode conter vários tamanhos diferentes da mesma imagem de ícone. Esses bits especificam o tamanho da imagem de ícone a ser carregada. Se nenhum dos bits estiver definido, a primeira imagem será carregada. Se apenas **msidbControlAttributesIconSize16** for definido, a primeira imagem de 16x16 será carregada. Se apenas o **msidbControlAttributesIconSize32** for definido, a primeira imagem 32x32 será carregada. Se **msidbControlAttributesIconSize48** for definido, a primeira imagem 48x48 será carregada.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Ícone](icon-control.md)

[Botão](pushbutton-control.md)

[Botão de opção](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Descrição                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua os bits de ícones na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Se o bit [FixedSize](fixedsize-control-attribute.md) não for definido, a imagem carregada será reduzida ou ampliada para se ajustar ao controle de ícone. Se o bit [FixedSize](fixedsize-control-attribute.md) for definido e a imagem carregada for menor do que o controle de ícone, a imagem será exibida centralizada dentro do controle. Se o bit [FixedSize](fixedsize-control-attribute.md) for definido e a imagem carregada for maior que o controle de ícone, a imagem será reduzida para se ajustar ao controle.

Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).

 

 



