---
description: Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de opção, o botão será desenhado com a aparência de um botão de ação, mas sua lógica permanecerá a mesma. Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Atributo de controle PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760834"
---
# <a name="pushlike-control-attribute"></a>Atributo de controle PushLike

Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de opção, o botão será desenhado com a aparência de um botão de ação, mas sua lógica permanecerá a mesma. Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.

## <a name="valid-controls"></a>Controles válidos

[](checkbox-control.md)[Botão de opção](radiobuttongroup-control.md) de caixa de seleção

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit PushLike na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



