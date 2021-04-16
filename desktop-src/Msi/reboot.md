---
description: A propriedade reboot suprime determinados prompts para uma reinicialização do sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reinicializar Propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747740"
---
# <a name="reboot-property"></a>Reinicializar Propriedade

A propriedade **reboot** suprime determinados prompts para uma reinicialização do sistema. Um administrador normalmente usa essa propriedade com uma série de instalações para instalar vários produtos ao mesmo tempo com apenas uma reinicialização no final. Para obter mais informações, consulte [reinicializações do sistema](system-reboots.md).

As ações [ForceReboot](forcereboot-action.md) e [ScheduleReboot](schedulereboot-action.md) informam o instalador para solicitar que o usuário reinicie o sistema. O instalador também pode determinar que uma reinicialização é necessária se houver alguma ação ForceReboot ou ScheduleReboot na sequência. Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos em uso durante a instalação.

Você pode suprimir determinados prompts para reinicializações definindo a propriedade **reboot** da seguinte maneira.



| Valor de reinicialização   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Sempre solicitar uma reinicialização no final da instalação. A IU sempre solicita ao usuário uma opção para reiniciar no final. Se não houver nenhuma interface do usuário e essa não for uma [instalação de vários pacotes](multiple-package-installations.md), o sistema será reiniciado automaticamente no final da instalação. Se esta for uma instalação de vários pacotes, não haverá reinicialização automática do sistema e o instalador retornará o \_ erro \_ reinicialização bem-sucedida \_ necessária. |
| Suprimir       | Suprimir prompts para uma reinicialização no final da instalação. O instalador ainda solicita ao usuário uma opção para reiniciar durante a instalação sempre que encontrar a [ação ForceReboot](forcereboot-action.md). Se não houver nenhuma interface do usuário, o sistema será reiniciado automaticamente em cada ForceReboot. As reinicializações no final da instalação (por exemplo, causada por uma tentativa de instalar um arquivo em uso) são suprimidas.                                    |
| ReallySuppress | Suprimir todas as reinicializações e solicitações de reinicialização iniciadas pelo ForceReboot durante a instalação. Suprimir todas as reinicializações e solicitações de reinicialização no final da instalação. O prompt de reinicialização e a reinicialização em si são suprimidos. Por exemplo, as reinicializações no final da instalação, causadas por uma tentativa de instalar um arquivo em uso, são suprimidas.                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O instalador só avalia o primeiro caractere da propriedade **reboot** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**Propriedade REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> </dl>

 

 




