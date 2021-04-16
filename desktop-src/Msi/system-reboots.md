---
description: O Windows Installer pode determinar quando uma reinicialização do sistema é necessária e solicitar automaticamente que o usuário seja reinicializado no final da instalação.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Reinicializações do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750592"
---
# <a name="system-reboots"></a>Reinicializações do sistema

O Windows Installer pode determinar quando uma reinicialização do sistema é necessária e solicitar automaticamente que o usuário seja reinicializado no final da instalação. Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos que estão em uso durante a instalação.

Os aplicativos que usam [Windows Installer](windows-installer-portal.md) versão 4,0 ou posterior para instalação e manutenção automaticamente usam o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) para reduzir as reinicializações do sistema. Windows Installer versão 4,0 ou posterior tem propriedades e políticas que permitem que o autor do pacote e os administradores controlem a interação de Windows Installer com o Gerenciador de reinicialização. Para obter mais informações, consulte [usando Windows Installer com o Gerenciador de reinicialização](using-windows-installer-with-restart-manager.md).

Os autores de pacotes de instalação podem agendar e suprimir reinicializações usando ações padrão nas tabelas de sequência e definindo propriedades. As seguintes ações e propriedades são usadas para lidar com reinicializações do sistema.



| Ação, caixa de diálogo ou propriedade                                                | Breve descrição                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ação ForceReboot](forcereboot-action.md)                                   | Solicita uma reinicialização do usuário durante a instalação.                                                                                                        |
| [Ação ScheduleReboot](schedulereboot-action.md)                             | Solicita ao usuário uma reinicialização no final da instalação.                                                                                                 |
| [**Reinicializar Propriedade**](reboot.md)                                              | Força ou suprime determinados prompts automáticos para uma reinicialização do sistema.                                                                                           |
| [**Propriedade REBOOTPROMPT**](rebootprompt.md)                                  | Suprime a exibição de prompts para reinicializações para o usuário. Todas as reinicializações necessárias acontecem automaticamente.                                                           |
| [**Propriedade AFTERREBOOT**](afterreboot.md)                                    | Normalmente usado em uma condição imposta pela ação ForceReboot.                                                                                               |
| [Ação InstallValidate](installvalidate-action.md)                           | Exibe a caixa de diálogo FilesInUse, se necessário, dando aos usuários a oportunidade de desligar os processos e evitar algumas reinicializações do sistema.                              |
| [Caixa de diálogo FilesInUse](filesinuse-dialog.md)                                     | Dá aos usuários a oportunidade de desligar processos para evitar algumas reinicializações do sistema.                                                                              |
| [Caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Dá aos usuários a opção de usar o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) para fechar e reiniciar aplicativos. Disponível a partir do Windows Installer versão 4,0. |
| [**Propriedade ReplacedInUseFiles**](replacedinusefiles.md)                      | Defina se o instalador é instalado em um arquivo em uso. Essa propriedade é usada por ações personalizadas para detectar que uma reinicialização é necessária.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Propriedade para desabilitar a interação de Windows Installer com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md). Disponível a partir do Windows Installer versão 4,0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Especifica como o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) fecha e reinicia os aplicativos. Disponível a partir do Windows Installer versão 4,0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Especifica como o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) fecha e reinicia os aplicativos. Disponível a partir do Windows Installer versão 4,0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | O instalador definirá essa propriedade se uma reinicialização do sistema operacional estiver pendente. Disponível a partir do Windows Installer versão 4,0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Política para desabilitar a interação de Windows Installer com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md). Disponível a partir do Windows Installer versão 4,0.                |



 

ERRO \_ \_ de instalação suspensa significa que a instalação não foi concluída ou revertida. A instalação deve ser retomada antes de ser concluída. O sistema pode precisar ser reinicializado para que a instalação possa ser retomada.

O Windows Installer retorna o erro de código de erro \_ instalar \_ suspender quando a [ação ForceReboot](forcereboot-action.md) for executada. Ela retornará \_ um erro \_ de reinicialização \_ de êxito necessária se uma reinicialização for necessária antes de executar o aplicativo e retornar um erro de \_ \_ reinicialização \_ com êxito iniciado se o instalador realmente tiver iniciado uma reinicialização. Observe que, como as reinicializações são assíncronas, a reinicialização pode realmente ocorrer antes que o código de erro seja retornado. Para obter mais informações, consulte [códigos de erro](error-codes.md).

Ações personalizadas podem forçar um prompt para reinicialização no final de uma instalação chamando [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). As ações personalizadas também podem verificar um prompt de reinicialização pendente chamando [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode).

## <a name="filesinuse-dialog"></a>Caixa de diálogo FilesInUse

O instalador pode determinar quando uma reinicialização do sistema é necessária e solicita ao usuário uma solicitação para reinicializar. Normalmente, uma reinicialização do sistema é necessária porque o instalador está tentando instalar um arquivo que está sendo usado no momento. Se a [ação InstallValidate](installvalidate-action.md) detectar a instalação de um arquivo em uso, ela exibirá a [caixa de diálogo FilesInUse](filesinuse-dialog.md).

Se você espera que o instalador exiba um FilesInUseDialog, mas ele não faz isso, isso pode ser devido a um dos seguintes motivos:

-   Os arquivos em uso não são executáveis.
-   O instalador não está realmente tentando instalar esses arquivos.
-   O processo que mantém esses arquivos é o processo que invoca a instalação.
-   O processo que contém esses arquivos é aquele que não tem uma janela com um título associado a ele.

Para obter mais informações, consulte [log de solicitações de reinicialização](logging-of-reboot-requests.md).

 

 
