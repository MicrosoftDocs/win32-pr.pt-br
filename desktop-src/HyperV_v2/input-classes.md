---
description: Os dispositivos de entrada do usuário são representados por essas classes. Uma máquina virtual sempre tem uma instância de cada classe associada a ela.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classes de entrada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df9c5a2f1d2743e062cf685dc6fd849f33333808315459560dfd840e925135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644858"
---
# <a name="input-classes"></a>Classes de entrada

Os dispositivos de entrada do usuário são representados por essas classes. Uma máquina virtual sempre tem uma instância de cada classe associada a ela. Esses dispositivos podem não ser adicionados ou removidos da máquina virtual. Portanto, não há nenhuma instância do pool de recursos para dispositivos de teclado ou mouse.

Os dispositivos de teclado e mouse são vinculados à máquina virtual por meio da Associação [**Msvm \_ SystemDevice**](msvm-systemdevice.md) . Uma máquina virtual contém um dispositivo de mouse PS2 e sintético. Somente um dispositivo apontador está ativo por vez.

Veja a seguir as classes WMI de virtualização relacionadas à entrada.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                          | Descrição                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**\_Teclado Msvm**](msvm-keyboard.md)<br/>             | Representa um dispositivo de teclado.<br/>        |
| [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Representa um dispositivo de mouse PS2.<br/>       |
| [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Representa um dispositivo de mouse sintético.<br/> |



 

 

 




