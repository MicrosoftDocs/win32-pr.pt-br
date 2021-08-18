---
description: A caixa de diálogo MsiRMFilesInUse pode ser escrita para exibir uma lista de processos que estão executando arquivos que precisam ser substituídos ou excluídos pela instalação.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Caixa de diálogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04aa3167609693135e2d3196fef0495d5244fe44f1a6e7d95d11f999efe51a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012884"
---
# <a name="msirmfilesinuse-dialog"></a>Caixa de diálogo MsiRMFilesInUse

A caixa de diálogo MsiRMFilesInUse pode ser escrita para exibir uma lista de processos que estão executando arquivos que precisam ser substituídos ou excluídos pela instalação. O usuário pode selecionar entre opções para "Fechar automaticamente aplicativos e reiniciá-los" ou "Não fechar aplicativos. (Uma reinicialização será necessária.)" Se o usuário selecionar a opção "Fechar automaticamente aplicativos e reiniciá-los", um controle de botão de push nessa caixa de diálogo poderá ser autor para publicar o evento de controle RMShutdownAndRestart e o [Gerenciador](../rstmgr/restart-manager-portal.md) de Reinicialização poderá fechar os aplicativos e reiniciá-los no final da instalação. Isso pode eliminar ou reduzir a necessidade de reiniciar o computador. Para obter mais informações, consulte [Reinicializações do sistema.](system-reboots.md)

A **caixa de diálogo MsiRMFilesInUse** será exibida durante uma instalação somente se todas as opções a seguir são verdadeiras. Quando qualquer um deles for false, o Windows instalador ignorará a caixa de **diálogo MsiRMFilesInUse.**

-   Uma versão do Windows Installer que não é anterior à versão 4.0 e um sistema operacional que não seja anterior ao Windows Vista ou ao Windows Server 2008 está executando a instalação.
-   O nível de interface do [usuário completo da interface](user-interface-levels.md) do usuário é usado.
-   As interações com o [Gerenciador](../rstmgr/restart-manager-portal.md) de Reinicialização não foram desabilitadas pela [**propriedade MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   A **caixa de diálogo MsiRMFilesInUse** está presente no pacote de instalação.
-   Todas as chamadas do instalador Windows para o Gerenciador de Reinicialização são [bem-sucedidas.](../rstmgr/restart-manager-portal.md)

Essa caixa de diálogo será criada conforme exigido pela [ação InstallValidate](installvalidate-action.md).

 

 
