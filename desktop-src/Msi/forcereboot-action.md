---
description: A ação ForceReboot solicita ao usuário uma reinicialização do sistema durante a instalação.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Ação ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41af6b656222a31ab75c9df3f2fa9f94af415f94d6d0b50010c0b25c5742502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636067"
---
# <a name="forcereboot-action"></a>Ação ForceReboot

A ação ForceReboot solicita ao usuário uma reinicialização do sistema durante a instalação. A ação ForceReboot é diferente da [ação ScheduleReboot](schedulereboot-action.md) , pois a ação ScheduleReboot é usada para agendar uma solicitação para reiniciar no final da instalação.

Se a instalação tiver uma interface do usuário, o instalador exibirá uma caixa de diálogo em cada ação ForceReboot que solicita que o usuário reinicie o sistema. O usuário deve responder a esse prompt antes de continuar com a instalação. Se a instalação não tiver nenhuma interface do usuário, o sistema será reiniciado automaticamente na ação ForceReboot.

Se o instalador determinar que uma reinicialização é necessária, ele solicitará automaticamente que o usuário seja reiniciado no final da instalação, independentemente de haver ou não ações ForceReboot ou ScheduleReboot na sequência. Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos usados durante a instalação.

Suprimir determinados prompts de reinicialização definindo a propriedade [**reboot**](reboot.md) .

se o Windows Installer encontrar a ação ForceReboot ou [ScheduleReboot](schedulereboot-action.md) durante uma [instalação de vários pacotes](multiple-package-installations.md), o instalador irá parar e reverter a instalação. Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.

## <a name="sequence-restrictions"></a>Restrições de sequência

As ações a seguir geralmente ocorrem juntas como um grupo na sequência de ação. É recomendável que a ação ForceReboot seja agendada para vir após esse grupo. Se a ação ForceReboot estiver agendada antes da [ação RegisterProduct](registerproduct-action.md), o instalador novamente exigirá a origem do pacote de instalação após a reinicialização. Portanto, a sequência preferida para ForceReboot é imediatamente após essa sequência de ação.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [Createatalhos](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

A ação ForceReboot deve vir entre [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) na sequência de ação da [tabela InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação ForceReboot sempre deve ser usada com uma instrução condicional de modo que o instalador dispare uma reinicialização somente quando necessário. Por exemplo, uma reinicialização só poderá ser necessária se um determinado arquivo for substituído ou se um componente específico estiver instalado. Cada instalação de produto é exclusiva e uma ação personalizada pode ser necessária para determinar se uma reinicialização é necessária. A condição na ação ForceReboot normalmente usa a propriedade [**AFTERREBOOT**](afterreboot.md) .

ForceReboot executa operações do sistema geradas por quaisquer ações anteriores antes de solicitar uma reinicialização ou reinicialização. Por exemplo, as operações do sistema geradas por [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) são executadas antes de uma reinicialização.

A ação ForceReboot grava uma chave do registro que faz com que o instalador seja iniciado após a reinicialização. o local dessa chave é **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reinicializações do sistema](system-reboots.md)
</dt> </dl>

 

 



