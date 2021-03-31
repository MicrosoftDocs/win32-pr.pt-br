---
description: A lista a seguir descreve as áreas de recursos novas e atualizadas para o Windows Server 2012 e o Windows Server 2012 R2. Para obter mais informações sobre as novas tecnologias do Windows 8 e do Windows 8.1, consulte tecnologias do Windows 8 e do Windows 8.1.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'O que há de novo: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829141"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>O que há de novo: Windows Server 2012 R2 & Windows Server 2012

A lista a seguir descreve as áreas de recursos novas e atualizadas para o Windows Server 2012 e o Windows Server 2012 R2. Para obter mais informações sobre as novas tecnologias do Windows 8 e do Windows 8.1, consulte [tecnologias do Windows 8 e do Windows 8.1](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>O que há de novo no Windows Server 2012 R2

-   [Eliminação de Duplicação de Dados](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    A eliminação de duplicação de dados localiza e remove a duplicação nos dados em um volume, garantindo que os dados permaneçam corretos e concluídos. Com isso, é possível armazenar mais dados de arquivo em menos espaço no volume. Para o Windows Server 2012 R2, vários parâmetros e códigos de erro foram ativados e a classe [**MSFT \_ DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) foi adicionada.

-   [Log de Inventário de Software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Novo!** O log de inventário de software coleta dados de licenciamento sobre o software instalado em um servidor Windows e fornece acesso remoto aos dados para que possam ser agregados facilmente por um datacenter.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    A API do servidor de destino iSCSI fornece provedores de Instrumentação de Gerenciamento do Windows (WMI) para gerenciar o servidor de destino Microsoft iSCSI, como a criação de discos virtuais e para apresentá-los ao cliente. Vários novos recursos foram adicionados ao Windows Server 2012 R2.

-   [Registro de gerenciamento de dispositivo móvel](../mdmreg/mobile-device-management-registration-portal.md)

    **Novo!** Uma tendência do setor foi desenvolver em que os funcionários conectam seus dispositivos pessoais de computação móvel à rede corporativa e aos recursos (no local ou por meio da nuvem) para executar tarefas de local de trabalho. Essa tendência exige suporte para uma configuração fácil da rede e dos recursos, de modo que os funcionários possam registrar dispositivos pessoais com a empresa para fins relacionados ao trabalho. Os aplicativos e a tecnologia para dar suporte à configuração fácil também devem permitir que os profissionais de ti gerenciem o risco associado à presença de dispositivos não controlados conectados à rede corporativa. O registro de MDM (gerenciamento de dispositivo móvel) registra um dispositivo em um serviço de gerenciamento.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    O Windows PowerShell é um shell de linha de comando baseado em tarefa e uma linguagem de script desenvolvida especialmente para a administração do sistema. Novidade no Windows Server 2012 R2, o Windows PowerShell v4 dá suporte à configuração de estado desejado, que é uma nova plataforma de gerenciamento no Windows PowerShell que permite a implantação e o gerenciamento de dados de configuração para serviços de software e o gerenciamento do ambiente no qual esses serviços são executados.

## <a name="whats-new-for-windows-server-2012"></a>O que há de novo no Windows Server 2012

-   [Clustering do Windows](/previous-versions/windows/desktop/mscs/windows-clustering)

    O clustering do Windows permite que você gerencie clusters com balanceamento de carga de rede, bem como clusters de failover. Vários novos recursos foram adicionados nesta versão, incluindo novos recursos de gerenciamento de grupo, propriedades comuns e integração com o WMI.

-   [Log de acesso do usuário](/previous-versions/windows/desktop/ual/user-access-logging)

    **Novo!** O registro de acesso do usuário (UAL) é uma estrutura comum para funções do Windows Server para relatar suas respectivas métricas de consumo. Essa estrutura UAL é um componente fundamental e essencial da solução de gerenciamento de licenciamento maior.

-   [Gerenciamento Remoto do Windows](../winrm/portal.md)

    O WinRM é a implementação da Microsoft do Protocolo WS-Management, um protocolo padrão amigável para firewall, baseado em SOAP (Simple Object Access Protocol), que permite que hardware e sistemas operacionais, de fornecedores diferentes, interoperem. O Windows Server 2012 inclui várias APIs de conexão que se concentram na interação com as instâncias e os shells em execução.

-   [Infraestrutura de gerenciamento do Windows](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Novo!** Os recursos de MI (infraestrutura de gerenciamento do Windows) representam a versão mais recente das tecnologias de Instrumentação de Gerenciamento do Windows (WMI), que se baseiam no padrão CIM da DMTF (força de tarefa de gerenciamento distribuído). A MI é totalmente compatível com as versões anteriores do WMI e fornece um host de recursos e benefícios que facilitam ainda mais o projeto e o desenvolvimento de provedores e clientes.

-   [Eliminação de Duplicação de Dados](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Novo!** A eliminação de duplicação de dados localiza e remove a duplicação nos dados em um volume, garantindo que os dados permaneçam corretos e concluídos. Com isso, é possível armazenar mais dados de arquivo em menos espaço no volume.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Novo!** A API do servidor de destino iSCSI fornece provedores de Instrumentação de Gerenciamento do Windows (WMI) para gerenciar o servidor de destino Microsoft iSCSI, como a criação de discos virtuais e para apresentá-los ao cliente.

-   [Provedor de NFS para WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Novo!** O provedor WMI de NFS fornece um meio de gerenciamento de configurações de cliente e servidor NFS, compartilhamentos de arquivos, netgroups e grupos de clientes.

-   [Arquivos Offline](../devnotes/offline-files.md)

    A API Arquivos Offline permite que os aplicativos controlem e monitorem o comportamento de Arquivos Offline programaticamente. O Windows Server 2012 adiciona as funções [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) e [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Gerenciamento de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Novo!** A API de gerenciamento de SMB fornece classes e métodos WMI para gerenciar compartilhamentos e compartilhar o acesso.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    O Windows Server fornece opções mínimas de instalação de servidor para computadores em execução no sistema operacional Windows Server 2008 ou posterior. O Windows Server 2012 oferece o Server Core como uma configuração, bem como as opções de instalação.

-   [Backup do Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    O recurso Backup do Windows Server automaticamente faz o backup e restaura os dados do aplicativo. O Windows Server 2012 inclui a API do provedor de backup de nuvem.

-   [Compartilhamento de área de trabalho do Windows](/previous-versions/windows/desktop/rdp/rdp-portal)

    O compartilhamento de área de trabalho do Windows é uma tecnologia de compartilhamento de tela de várias partes. O Windows Server 2012 implementa essa tecnologia usando a API de duplicação do Windows.

-   [Serviços de área de trabalho remota](../termserv/terminal-services-portal.md)

    O compartilhamento de área de trabalho do Windows permite que o usuário acesse remotamente uma instância do sistema operacional. O Windows Server 2012 inclui vários recursos novos, incluindo sessões filhas, redirecionamento de mídia do RemoteFX e cliente do agente de Área de Trabalho Remota.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    O Windows PowerShell é um shell de linha de comando baseado em tarefa e uma linguagem de script desenvolvida especialmente para a administração do sistema. Novidade no Windows Server 2012, o Windows PowerShell v3 dá suporte ao fluxo de trabalho do Windows PowerShell, que aproveita os benefícios do Windows Workflow Foundation para permitir a automação de tarefas de longa execução.

-   [OData de gerenciamento](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Novo!** Também conhecido como serviços Web do Windows PowerShell, o Management OData, novo no Windows PowerShell v3, permite a criação de um ponto de extremidade de serviço Web ASP.NET que expõe dados de gerenciamento, Aces enpostas por meio de comandos do Windows PowerShell, como entidades de serviço Web OData.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Server 2012 R2 no TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 e Windows Server 2012 na biblioteca do TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 no Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
