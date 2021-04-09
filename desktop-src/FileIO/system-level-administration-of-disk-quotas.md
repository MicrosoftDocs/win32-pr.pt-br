---
description: O administrador do sistema pode definir cotas para usuários específicos em um volume. O administrador também pode definir as cotas padrão para o volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administração em nível de sistema de cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164643"
---
# <a name="system-level-administration-of-disk-quotas"></a>Administração em nível de sistema de cotas de disco

O administrador do sistema pode definir cotas para usuários específicos em um volume. O administrador também pode definir as cotas padrão para o volume. Um novo usuário no volume recebe a cota padrão, a menos que o administrador tenha estabelecido uma cota especificamente para esse usuário.

O administrador pode consultar o nível de controle de cotas e imposição (ou Estados de cota), os limites de cota padrão e as informações de cota por usuário. As informações de cota por usuário contêm o limite de cota rígido do usuário, o limite de aviso e o uso da cota. O administrador também pode habilitar ou desabilitar a imposição de cotas.

Há três Estados de cota, conforme mostrado na tabela a seguir.



| Estado          | Descrição                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cota desabilitada | As alterações de uso de cota não são rastreadas, mas os limites de cota não são removidos. Nesse estado, o desempenho não é afetado pelas cotas de disco. Esse é o valor padrão.                         |
| Cota controlada  | As alterações de uso de cota são controladas, mas os limites de cota não são impostos. Nesse estado, nenhum evento de violação de cota é gerado e nenhuma operação de arquivo falha devido a violações de cota de disco. |
| Cota imposta | As alterações de uso de cota são rastreadas e os limites de cota são impostos.                                                                                                                           |



 

 

 



