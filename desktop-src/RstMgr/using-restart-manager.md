---
title: Usando o Gerenciador de reinicialização
description: As seções a seguir descrevem o uso da API do Gerenciador de reinicialização.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Gerente de reinicialização do Gerenciador de reinicialização usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90826091aa4a3cdf39e0a1f063a211255ec4ef9cf84b06214eb172150ac3b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009994"
---
# <a name="using-restart-manager"></a>Usando o Gerenciador de reinicialização

As seções a seguir descrevem o uso da API do Gerenciador de reinicialização. Seus aplicativos e serviços também devem seguir as [diretrizes para aplicativos e serviços](guidelines-for-applications-and-services.md).

## <a name="using-the-microsoft-windows-installer"></a>usando o Microsoft Windows Installer

o [Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4,0 é o serviço de instalação de aplicativo do Windows Vista ou Windows Server 2008. os aplicativos que usam o Windows Installer versão 4,0 para instalação e manutenção automaticamente usam o gerenciador de reinicialização para reduzir as reinicializações do sistema. Instaladores personalizados também podem ser criados para chamar a API do Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços diretamente para evitar a necessidade de uma reinicialização do sistema. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a função [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) para agendá-lo de forma que ele Minimize a interrupção para o usuário. os pacotes interativos Windows Installer devem implementar uma interface do usuário que inclua uma caixa de diálogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) . para obter mais informações, consulte [usando Windows Installer com o gerenciador de reinicialização](/windows/desktop/Msi/using-windows-installer-with-restart-manager) na documentação do SDK do Windows Installer.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Usando a API do Gerenciador de reinicialização com instaladores personalizados

instaladores personalizados, ou um pacote Windows Installer que contém ações personalizadas que causam uma reinicialização do sistema, podem usar a API do gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços.

-   Todas as operações executadas usando a API do Gerenciador de reinicialização devem ser associadas a uma sessão. Um máximo de 64 sessões do Gerenciador de reinicialização por sessão do usuário pode ser aberto no sistema ao mesmo tempo. O instalador primário inicia e termina a sessão do Gerenciador de reinicialização. Para obter mais informações sobre como usar o Gerenciador de reinicialização com um único instalador, consulte [usando o Gerenciador de reinicialização com um instalador primário](using-restart-manager-with-a-primary-installer.md).
-   Se necessário para a instalação, um ou mais instaladores secundários podem ser associados à sessão do Gerenciador de reinicialização e podem ser executados em processo ou fora do processo do instalador primário. Os instaladores secundários exigem que a chave de sessão seja fornecida pelo instalador primário para ingressar em uma sessão. Para obter mais informações e um exemplo de como usar instaladores secundários, consulte [usando o Gerenciador de reinicialização com um instalador secundário](using-restart-manager-with-a-secondary-installer.md).
-   Os instaladores interativos devem implementar uma interface do usuário que inclua uma caixa de diálogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) que possa pedir aos usuários que fechem aplicativos e serviços. para obter mais informações, consulte [usando Windows Installer com o gerenciador de reinicialização](/windows/desktop/Msi/using-windows-installer-with-restart-manager) na documentação do SDK do Windows Installer.
-   Os instaladores podem chamar a API do Gerenciador de reinicialização para alterar, cancelar e obter o status da operação do Gerenciador de reinicialização atual. Para obter mais informações, consulte os seguintes tópicos: [obtendo o status de uma operação do Gerenciador de reinicialização](getting-the-status-of-a-restart-manager-operation.md) e [cancelando a operação atual do Gerenciador de reinicialização](canceling-the-current-restart-manager-operation.md).
-   Os instaladores não devem desabilitar o redirecionamento do sistema de arquivos antes de chamar a API do Gerenciador de reinicialização. alguns instaladores de 32 bits executados em 64 bits Windows podem não conseguir registrar um arquivo no diretório% windir% \\ system32.

 

 