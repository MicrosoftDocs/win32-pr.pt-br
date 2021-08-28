---
description: Se esse bit for definido, o controle será exibido com uma aparência de três dimensões e esnoque.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de controle de sunken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3547f06d82a66a08a575958eac728051c3315f3382529065c3792cfdb94def
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626926"
---
# <a name="sunken-control-attribute"></a>Atributo de controle de sunken

Se esse bit for definido, o controle será exibido com uma aparência de três dimensões e esnoque. O efeito desse bit de estilo é diferente em diferentes controles e versões do Windows. Em alguns controles, ele não tem nenhum efeito visível. Se o sistema não dá suporte ao atributo de controle Sunken, o controle é exibido no estilo visual padrão. Se esse bit não estiver definido, o controle será exibido com o estilo visual padrão.

## <a name="valid-controls"></a>Controles válidos

Todos os controles.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit de sunken na coluna Atributos do registro do controle na [tabela Controle](control-table.md).

Consulte [Controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



