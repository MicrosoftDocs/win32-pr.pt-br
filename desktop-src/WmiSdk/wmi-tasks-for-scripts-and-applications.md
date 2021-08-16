---
description: Descreve como encontrar a classe e os procedimentos corretos do WMI a serem usados em scripts e aplicativos que executam tarefas comuns de administração de computador e rede.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Tarefas do WMI para scripts e aplicativos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d273db41b832b8141fe13bdf0538b51fb221688949792e214c9f81c1e7b96e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553120"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Tarefas do WMI para scripts e aplicativos

As seções a seguir descrevem várias tarefas de administração de computador e rede e fornecem links para a classe WMI ou classes usadas para executar essas tarefas. Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md). Para obter mais informações sobre como usar o WMI, consulte [mais informações](further-information.md). Para obter mais informações sobre como usar o WMI, consulte [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Esses recursos podem não estar disponíveis em todos os idiomas ou países/regiões.)

Para obter mais informações sobre como fornecer dados ao WMI, consulte [usando o WMI](using-wmi.md), que fará referência a tópicos sobre como gravar um [*provedor*](gloss-p.md)WMI.

As operações mostradas nos exemplos de script podem ser executadas por aplicativos em C++ ou Visual Basic. Para obter mais informações, consulte [criando um aplicativo WMI usando](creating-a-wmi-application-using-c-.md) os [exemplos de aplicativos C++ e WMI c++](wmi-c---application-examples.md).

A tabela a seguir lista as categorias de tarefas.



| Categorias de Tarefa                                                               | Descrição                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contas e domínios](wmi-tasks--accounts-and-domains.md)                   | Obtenha informações como o domínio do computador ou o usuário conectado no momento. Muitas tarefas relacionadas a domínio ou conta são mais bem executadas com scripts [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) . Para obter exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware de Computador](wmi-tasks--computer-hardware.md)                         | Obtenha informações sobre a presença, o estado ou as propriedades de componentes de hardware. Por exemplo, você pode determinar se um computador é um desktop ou um laptop.                                                                                                                                                                                             |
| [Software de computador](wmi-tasks--computer-software.md)                         | obtenha informações como qual software é instalado pelo Windows Installer (MSI) e pelas versões de software.                                                                                                                                                                                                                                              |
| [Conectando-se ao serviço WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Para obter dados do WMI, seja no computador local ou em um computador remoto, você deve se conectar ao serviço WMI conectando-se a um [*namespace*](gloss-n.md)específico. Na maioria dos casos, use a conexão de [moniker](creating-a-wmi-script.md) abreviada ou a conexão do [**localizador**](swbemlocator-connectserver.md) .    |
| [Datas e horas](wmi-tasks--dates-and-times.md)                             | Há classes WMI e um objeto de script para analisar ou converter o formato de [data e hora CIM](date-and-time-format.md) .                                                                                                                                                                                                                                     |
| [Gerenciamento de desktop](wmi-tasks--desktop-management.md)                       | Obtenha dados de ou controle áreas de trabalho remotas. Por exemplo, você pode determinar se a proteção de tela requer ou não uma senha. O WMI também oferece a capacidade de desligar um computador remoto.                                                                                                                                                               |
| [Discos e sistemas de arquivos](wmi-tasks--disks-and-file-systems.md)               | Obtenha informações sobre o estado do hardware da unidade de disco, volumes lógicos.                                                                                                                                                                                                                                                                                      |
| [Logs de eventos](wmi-tasks--event-logs.md)                                       | Obtenha dados de eventos de arquivos de log de eventos NT e execute operações como fazer backup ou limpar arquivos de log.                                                                                                                                                                                                                                                   |
| [Arquivos e pastas](wmi-tasks--files-and-folders.md)                         | Altere as propriedades de arquivo ou pasta por meio do WMI, incluindo a criação de um compartilhamento ou a renomeação de um arquivo.                                                                                                                                                                                                                                                              |
| [Rede](wmi-tasks--networking.md)                                       | Gerencie e obtenha informações sobre conexões e endereços IP ou MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemas Operacionais](wmi-tasks--operating-systems.md)                         | Obtenha informações sobre o sistema operacional, como a versão, se ele está ativado ou quais hotfixes estão instalados.                                                                                                                                                                                                                                  |
| [Monitoramento de desempenho](wmi-tasks--performance-monitoring.md)               | Use as classes WMI que obtêm dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador.                                                                                                                                                                                                                                     |
| [Processos](wmi-tasks--processes.md)                                         | Obtenha informações como a conta sob a qual um processo está sendo executado. Você pode executar ações como criar processos.                                                                                                                                                                                                                                 |
| [Impressoras e impressão](wmi-tasks--printers-and-printing.md)                 | Gerencie e obtenha dados sobre impressoras, como localizar ou definir a impressora padrão.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Criar e modificar chaves e valores do registro.                                                                                                                                                                                                                                                                                                               |
| [Tarefas agendadas](wmi-tasks--scheduled-tasks.md)                             | Crie e obtenha informações sobre as tarefas agendadas.                                                                                                                                                                                                                                                                                                         |
| [Serviços](wmi-tasks--services.md)                                           | Obtenha informações sobre serviços, incluindo serviços dependentes ou antecedentes.                                                                                                                                                                                                                                                                            |



 

 

 
