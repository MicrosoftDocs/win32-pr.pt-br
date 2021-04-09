---
description: Esse atributo adiciona o ícone de elevação do controle de conta de usuário (UAC) (ícone de escudo) ao controle de pressão.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091691"
---
# <a name="elevationshield-attribute"></a>Atributo ElevationShield

Esse atributo adiciona o ícone de elevação do [*controle de conta de usuário*](u-gly.md) (UAC) (ícone de escudo) ao controle de [pressão](pushbutton-control.md).

Se esse bit estiver definido e a instalação ainda não estiver sendo executada com privilégios [*elevados*](e-gly.md) , o controle de supressão será criado usando o ícone de elevação do UAC ( [*controle de conta de usuário*](u-gly.md) ) (ícone de escudo).

Se esse bit estiver definido e a instalação já estiver sendo executada com privilégios [*elevados*](e-gly.md) , o controle de supressão será criado usando os outros atributos de ícone.

Se esse bit não estiver definido, o controle de supressão será criado usando os outros atributos Icon.

## <a name="valid-controls"></a>Controles válidos

[Botão](pushbutton-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



