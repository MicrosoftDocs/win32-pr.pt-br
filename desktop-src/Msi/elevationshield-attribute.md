---
description: Esse atributo adiciona o ícone de elevação do UAC (Controle de Conta de Usuário) (ícone de blindagem) ao controle PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4c5da7133a7216386be56328c0e21e2e365129caa185e045984cb5e89b7d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637486"
---
# <a name="elevationshield-attribute"></a>Atributo ElevationShield

Esse atributo adiciona o [*ícone de*](u-gly.md) elevação do UAC (Controle de Conta de Usuário) (ícone de blindagem) ao [controle PushButton](pushbutton-control.md).

Se esse bit estiver definido e a [](e-gly.md) instalação ainda não estiver em execução com privilégios elevados, o controle pushbutton será criado usando o ícone de elevação do UAC [*(Controle*](u-gly.md) de Conta de Usuário) (ícone de blindagem).

Se esse bit estiver definido e a [](e-gly.md) instalação já estiver em execução com privilégios elevados, o controle pushbutton será criado usando os outros atributos de ícone.

Se esse bit não estiver definido, o controle pushbutton será criado usando os outros atributos de ícone.

## <a name="valid-controls"></a>Controles válidos

[Botão](pushbutton-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



