---
title: Sobre o Restart Manager
description: O principal motivo pelo qual a instalação e as atualizações de software exigem uma reinicialização do sistema é que alguns dos arquivos que estão sendo atualizados estão sendo usados atualmente por um aplicativo ou serviço em execução.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Restart Manager Restart Mgr , about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98003ff4193ce26eb4ed2a3bdab60db8d58adf86698c6b9369a80b8043458579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010293"
---
# <a name="about-restart-manager"></a>Sobre o Restart Manager

O principal motivo pelo qual a instalação e as atualizações de software exigem uma reinicialização do sistema é que alguns dos arquivos que estão sendo atualizados estão sendo usados atualmente por um aplicativo ou serviço em execução. O Restart Manager permite que todos os aplicativos e serviços críticos sejam desligados e reiniciados. Isso libera os arquivos que estão em uso e permite que as operações de instalação sejam concluídas. Ele também pode eliminar ou reduzir o número de reinicializações do sistema necessárias para concluir uma instalação ou atualização.

O Gerenciador de Reinicialização interrompe os aplicativos na ordem a seguir e, depois que os aplicativos são atualizados, reinicia os aplicativos que foram registrados para reinicialização na ordem inversa.

1.  Aplicativos de GUI
2.  Aplicativos de console
3.  Serviços Windows
4.  Windows explorer

O Gerenciador de Reinicialização desligará o aplicativo ou os serviços somente se o chamador tiver permissão para fazer isso. Observe que não há suporte para o desligamento entre sessões.

Os aplicativos que usam o [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4.0 para instalação e manutenção usam automaticamente o Gerenciador de Reinicialização para reduzir as reinicializações do sistema. Os instaladores personalizados também podem ser projetados para chamar a API do Gerenciador de Reinicialização para desligar e reiniciar aplicativos e serviços. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do Gerenciador de Reinicialização para agendar reinicializações de forma que minimize a interrupção do fluxo de trabalho do usuário.

Para obter informações sobre como usar a API do Gerenciador de Reinicialização durante a instalação e as atualizações, consulte [Usando o Gerenciador de Reinicialização](using-restart-manager.md).

Os serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de Reinicialização sem uma reinicialização do sistema. Para obter mais informações sobre como identificar serviços críticos do sistema, consulte [Critical System Services](critical-system-services.md).

Seus aplicativos e serviços devem estar preparados para serem desligados pelo Gerenciador de Reinicialização e salvar dados de usuário e informações de estado necessárias para uma reinicialização limpa. Para obter mais informações sobre como preparar seus aplicativos e serviços para trabalhar com o Gerenciador de Reinicialização, consulte [Diretrizes para aplicativos e serviços.](guidelines-for-applications-and-services.md)

Para obter informações de referência sobre as enumerações, estruturas e funções da API do Restart Manager, consulte a [seção Referência do Gerenciador de Reinicialização](restart-manager-reference.md)

 

 