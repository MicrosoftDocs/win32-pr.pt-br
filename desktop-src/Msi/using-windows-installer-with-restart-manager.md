---
description: Os aplicativos que usam o Windows Installer 4,0 para instalação e manutenção no Windows Vista usam automaticamente o Gerenciador de reinicialização para reduzir as reinicializações do sistema.
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: Usando Windows Installer com o Gerenciador de reinicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4160b2241c75ec7305accd1ab4d1295a54fa9f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785416"
---
# <a name="using-windows-installer-with-restart-manager"></a>Usando Windows Installer com o Gerenciador de reinicialização

Os aplicativos que usam o Windows Installer 4,0 para instalação e manutenção no Windows Vista usam automaticamente o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) para reduzir as reinicializações do sistema. O comportamento padrão no Windows Vista é desligar os aplicativos em vez de desligar e reiniciar o sistema operacional sempre que possível. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) para agendar reinicializações de forma a minimizar a interrupção do fluxo de trabalho do usuário.

Windows Installer os desenvolvedores podem executar as seguintes ações para preparar seu pacote para trabalhar com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md).

-   Adicione a caixa de diálogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) ao seu pacote. Se a caixa de diálogo MsiRMFilesInUse estiver presente no pacote, o usuário do Windows Vista que está executando uma instalação no [nível da interface do usuário](user-interface-levels.md) da interface de usuários completa terá a opção de fechar e reiniciar os aplicativos automaticamente. Um pacote de instalação pode conter informações para a caixa de diálogo MsiRMFilesInUse e para a caixa de diálogo [FilesInUse](filesinuse-dialog.md) . A caixa de diálogo MsiRMFilesInUse só será exibida se o pacote for instalado com pelo menos Windows Installer 4,0 no Windows Vista e, caso contrário, será ignorado. Os pacotes existentes que não têm a caixa de diálogo MsiRMFilesInUse continuam a funcionar usando a caixa de diálogo FilesInUse. Uma transformação de personalização pode ser usada para adicionar uma caixa de diálogo MsiRMFilesInUse a pacotes existentes.

    Normalmente, os usuários finais executam instalações no nível completo da [interface do usuário](user-interface-levels.md)da IU. Interface do usuário básica ou instalações reduzidas no nível da interface do usuário oferecem aos usuários a opção de usar o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) para reduzir as reinicializações do sistema, mesmo que a caixa de diálogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) não esteja presente. Instalações silenciosas em nível de interface do usuário sempre desligam aplicativos e serviços e, no Windows Vista, sempre usam o Gerenciador de reinicialização.

-   Registre aplicativos para uma reinicialização usando a função [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . O Gerenciador de reinicialização só pode reiniciar os aplicativos que foram registrados para reinicialização. O Restart Manager reinicia os aplicativos registrados após a instalação. Se a instalação exigir uma reinicialização do sistema, o Gerenciador de reinicialização reiniciará o aplicativo registrado após a reinicialização do sistema.
-   Especifique INSTALLLOGMODE \_ RMFILESINUSE ao habilitar um manipulador de interface de usuário externo com as funções [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) e [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) . Windows Installer enviará uma \_ mensagem INSTALLMESSAGE RMFILESINUSE para manipuladores de interface do usuário externos que dão suporte ao [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md). Se nenhuma interface de usuário registrada ou interna manipular a \_ mensagem INSTALLMESSAGE RMFILESINUSE, o instalador enviará uma \_ mensagem INSTALLMESSAGE FILESINUSE para manipuladores de interface do usuário que dão suporte à caixa de diálogo [FILESINUSE](filesinuse-dialog.md) . Para obter mais informações, consulte [usando o Gerenciador de reinicialização com uma interface do usuário externa](using-restart-manager-with-an-external-ui-.md).
-   As ações personalizadas podem adicionar recursos que pertencem a uma sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) . A ação personalizada deve ser sequenciada antes da ação [InstallValidate](installvalidate-action.md) . As ações personalizadas podem usar a propriedade [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md) para obter a chave de sessão e devem chamar as funções [**RmJoinSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) e [**RmEndSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) da API do Gerenciador de reinicialização. Ações personalizadas não podem remover recursos que pertencem a uma sessão do Gerenciador de reinicialização. As ações personalizadas não devem tentar desligar ou reiniciar aplicativos usando as funções [**RmShutdown**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown), [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) e [**RmRestart**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart) .
-   Os autores de pacote podem basear uma condição na [tabela LaunchCondition](launchcondition-table.md) na propriedade [**MsiSystemRebootPending**](msisystemrebootpending.md) para impedir a instalação do pacote quando uma reinicialização do sistema estiver pendente.
-   Os autores e os administradores de pacotes podem controlar a interação do Windows Installer e do Gerenciador de reinicialização usando as propriedades [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md), [**MSIDISABLERMRESTART**](msidisablermrestart.md), [**MSIRMSHUTDOWN**](msirmshutdown.md) e a política [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Os aplicativos e serviços devem seguir as diretrizes descritas na seção [usando o Gerenciador de reinicialização](../rstmgr/using-restart-manager.md) da documentação do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) .

 

 
