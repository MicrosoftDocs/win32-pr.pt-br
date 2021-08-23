---
description: Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de rádio, o botão será desenhado com a aparência de um botão de push, mas sua lógica permanecerá a mesma. Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Atributo de controle PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692467"
---
# <a name="pushlike-control-attribute"></a>Atributo de controle PushLike

Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de rádio, o botão será desenhado com a aparência de um botão de push, mas sua lógica permanecerá a mesma. Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit PushLike na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



