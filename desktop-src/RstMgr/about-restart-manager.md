---
title: Sobre o Gerenciador de reinicialização
description: O principal motivo pelo qual a instalação e as atualizações de software exigem uma reinicialização do sistema é que alguns dos arquivos que estão sendo atualizados estão sendo usados no momento por um aplicativo ou serviço em execução.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Restart Manager Restart Mgr, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641668"
---
# <a name="about-restart-manager"></a>Sobre o Gerenciador de reinicialização

O principal motivo pelo qual a instalação e as atualizações de software exigem uma reinicialização do sistema é que alguns dos arquivos que estão sendo atualizados estão sendo usados no momento por um aplicativo ou serviço em execução. O Gerenciador de reinicialização permite que todos os aplicativos e serviços críticos sejam desligados e reiniciados. Isso libera os arquivos que estão em uso e permite que as operações de instalação sejam concluídas. Ele também pode eliminar ou reduzir o número de reinicializações do sistema que são necessárias para concluir uma instalação ou atualização.

O Gerenciador de reinicialização interrompe os aplicativos na seguinte ordem e, depois que os aplicativos são atualizados, o reinicia os aplicativos que foram registrados para reinicialização na ordem inversa.

1.  Aplicativos de GUI
2.  Aplicativos de console
3.  Serviços Windows
4.  Windows Explorer

O Gerenciador de reinicialização desliga o aplicativo ou os serviços somente se o chamador tiver permissão para fazer isso. Observe que não há suporte para o desligamento entre sessões.

Os aplicativos que usam o [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4,0 para instalação e manutenção automaticamente usam o Gerenciador de reinicialização para reduzir as reinicializações do sistema. Instaladores personalizados também podem ser criados para chamar a API do Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços. Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do Gerenciador de reinicialização para agendar reinicializações de forma a minimizar a interrupção do fluxo de trabalho do usuário.

Para obter informações sobre como usar a API do Gerenciador de reinicialização durante a instalação e as atualizações, consulte [using Restart Manager](using-restart-manager.md).

Serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de reinicialização sem a reinicialização do sistema. Para obter mais informações sobre como identificar serviços críticos do sistema, consulte [serviços críticos do sistema](critical-system-services.md).

Seus aplicativos e serviços devem estar preparados para serem desligados pelo Gerenciador de reinicialização e salvar dados de usuário e informações de estado necessárias para uma reinicialização limpa. Para obter mais informações sobre como preparar seus aplicativos e serviços para trabalhar com o Gerenciador de reinicialização, consulte [diretrizes para aplicativos e serviços](guidelines-for-applications-and-services.md).

Para obter informações de referência sobre as enumerações, estruturas e funções da API do Gerenciador de reinicialização, consulte a seção de [referência do Gerenciador de reinicialização](restart-manager-reference.md)

 

 