---
description: Se esse bit for definido, o controle será exibido com uma aparência de baixo relevo, tridimensional.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de controle de baixo-relevo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090933"
---
# <a name="sunken-control-attribute"></a>Atributo de controle de baixo-relevo

Se esse bit for definido, o controle será exibido com uma aparência de baixo relevo, tridimensional. O efeito desse tipo de bit é diferente em diferentes controles e versões do Windows. Em alguns controles, ele não tem efeito visível. Se o sistema não oferecer suporte ao atributo de controle de baixo relevo, o controle será exibido no estilo visual padrão. Se esse bit não for definido, o controle será exibido com o estilo visual padrão.

## <a name="valid-controls"></a>Controles válidos

Todos os controles.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit de baixo e baixo na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



