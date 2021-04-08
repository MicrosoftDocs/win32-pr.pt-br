---
description: Insira a ação ScheduleReboot na sequência de ação para solicitar ao usuário uma reinicialização do sistema no final da instalação. Use a ação ForceReboot para solicitar uma reinicialização durante a instalação.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Ação ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828428"
---
# <a name="schedulereboot-action"></a>Ação ScheduleReboot

Insira a ação ScheduleReboot na sequência de ação para solicitar ao usuário uma reinicialização do sistema no final da instalação. Use a [ação ForceReboot](forcereboot-action.md) para solicitar uma reinicialização durante a instalação.

Se a instalação tiver uma interface do usuário, o instalador exibirá uma caixa de mensagem e um botão no final da instalação, perguntando se o usuário deseja reiniciar o sistema. O usuário deve responder a este prompt antes de concluir a instalação. Se a instalação não tiver nenhuma interface do usuário, o sistema será reiniciado automaticamente no final.

Se o instalador determinar que uma reinicialização é necessária, ele solicitará automaticamente que o usuário seja reiniciado no final da instalação, independentemente de haver ou não qualquer ação ForceReboot ou ScheduleReboot na sequência. Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos que estão em uso durante a instalação.

Você pode suprimir determinados prompts para reinicializações definindo a propriedade [**reboot**](reboot.md) .

Se o Windows Installer encontrar a ação [ForceReboot](forcereboot-action.md) ou ScheduleReboot durante uma [instalação de vários pacotes](multiple-package-installations.md), o instalador irá parar e reverter a instalação. Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Por exemplo, essa ação pode ser usada para forçar o instalador a solicitar uma reinicialização depois de instalar os drivers que exigem uma reinicialização. Se o instalador tentar substituir os arquivos que estão em uso, ele solicitará automaticamente que o usuário seja reiniciado mesmo que ScheduleReboot não tenha sido usado.

A ação ScheduleReboot normalmente é colocada no final da sequência, mas pode ser inserida em qualquer ponto na sequência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> </dl>

 

 



