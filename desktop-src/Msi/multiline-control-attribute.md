---
description: Se esse bit for definido em um controle de edição, o instalador criará um controle de edição de várias linhas com uma barra de rolagem vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de controle de várias linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165354"
---
# <a name="multiline-control-attribute"></a>Atributo de controle de várias linhas

Se esse bit for definido em um [controle de edição](edit-control.md), o instalador criará um controle de edição de várias linhas com uma barra de rolagem vertical.

Se esse bit não for definido, ele especificará a exibição de um controle de edição normal.

## <a name="valid-controls"></a>Controles válidos

[Controle de edição](edit-control.md).



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua o bit multilinha na coluna atributos do registro do controle na [tabela de controle](control-table.md).

Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



