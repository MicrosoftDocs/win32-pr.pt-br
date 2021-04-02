---
description: A caixa de diálogo MsiRMFilesInUse pode ser criada para exibir uma lista de processos que atualmente estão executando arquivos que precisam ser substituídos ou excluídos pela instalação.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Caixa de diálogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922742"
---
# <a name="msirmfilesinuse-dialog"></a>Caixa de diálogo MsiRMFilesInUse

A caixa de diálogo MsiRMFilesInUse pode ser criada para exibir uma lista de processos que atualmente estão executando arquivos que precisam ser substituídos ou excluídos pela instalação. O usuário pode selecionar entre opções para "fechar aplicativos automaticamente e reiniciá-los" ou "não fechar aplicativos. (Uma reinicialização será necessária.) " Se o usuário selecionar a opção "fechar aplicativos automaticamente e reiniciá-los", um controle de botão de ação nessa caixa de diálogo poderá ser criado para publicar o evento de controle RMShutdownAndRestart e o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) poderá fechar os aplicativos e reiniciá-los no final da instalação. Isso pode eliminar ou reduzir a necessidade de reiniciar o computador. Para obter mais informações, consulte [reinicializações do sistema](system-reboots.md).

A caixa de diálogo **MsiRMFilesInUse** será exibida durante uma instalação somente se todas as seguintes opções forem verdadeiras. Quando qualquer um desses for falso, o Windows Installer ignorará a caixa de diálogo **MsiRMFilesInUse** .

-   Uma versão Windows Installer que não seja anterior à versão 4,0 e um sistema operacional que não seja anterior ao Windows Vista ou ao Windows Server 2008 esteja executando a instalação.
-   O nível completo da [interface do usuário](user-interface-levels.md) da interface é usado.
-   As interações com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não foram desabilitadas pela propriedade [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   A caixa de diálogo **MsiRMFilesInUse** está presente no pacote de instalação.
-   Todas as chamadas do Windows Installer para o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) são bem-sucedidas.

Essa caixa de diálogo será criada conforme exigido pela [ação InstallValidate](installvalidate-action.md).

 

 
