---
description: Descreve como encontrar a classe e os procedimentos corretos do WMI a usar em scripts e aplicativos que executam tarefas comuns de administração de rede e computador.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Tarefas WMI para scripts e aplicativos
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
# <a name="wmi-tasks-for-scripts-and-applications"></a>Tarefas WMI para scripts e aplicativos

As seções a seguir descrevem várias tarefas de administração de rede e computador e fornecem links para a classe WMI ou classes usadas para executar essas tarefas. Para obter mais informações, consulte [Criando um aplicativo WMI ou script](creating-a-wmi-application-or-script.md). Para obter mais informações sobre como usar o WMI, consulte [Mais informações.](further-information.md) Para obter mais informações sobre como usar o WMI, consulte [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Esses recursos podem não estar disponíveis em cada idioma ou país/região.)

Para obter mais informações sobre como fornecer dados ao WMI, consulte [Usando wmi](using-wmi.md), que fará referência a tópicos sobre como escrever um provedor [*WMI*](gloss-p.md).

As operações mostradas em exemplos de script podem ser executadas por aplicativos em C++ ou Visual Basic. Para obter mais informações, consulte [Criando um aplicativo WMI usando exemplos](creating-a-wmi-application-using-c-.md) de aplicativo C++ e [WMI C++.](wmi-c---application-examples.md)

A tabela a seguir lista as categorias de tarefas.



| Categorias de Tarefa                                                               | Descrição                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contas e domínios](wmi-tasks--accounts-and-domains.md)                   | Obtenha informações como o domínio do computador ou o usuário conectado no momento. Muitas tarefas relacionadas ao domínio ou à conta são mais bem executadas com scripts [ADSI.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Para exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware de Computador](wmi-tasks--computer-hardware.md)                         | Obtenha informações sobre a presença, o estado ou as propriedades dos componentes de hardware. Por exemplo, você pode determinar se um computador é um desktop ou laptop.                                                                                                                                                                                             |
| [Software do computador](wmi-tasks--computer-software.md)                         | Obtenha informações como qual software é instalado pelo MSI (Instalador Windows) do Windows e versões de software.                                                                                                                                                                                                                                              |
| [Conectando-se ao serviço WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Para obter dados do WMI, seja no computador local ou em um computador remoto, você deve se conectar ao serviço WMI conectando-se a um [*namespace específico.*](gloss-n.md) Na maioria dos casos, use a conexão [de moniker](creating-a-wmi-script.md) de forma curta ou a [**conexão do Localizador.**](swbemlocator-connectserver.md)    |
| [Datas e horas](wmi-tasks--dates-and-times.md)                             | Há classes WMI e um objeto de script para analisar ou converter o [formato datetime cim.](date-and-time-format.md)                                                                                                                                                                                                                                     |
| [Gerenciamento de Área de Trabalho](wmi-tasks--desktop-management.md)                       | Obter dados de ou controlar áreas de trabalho remotas. Por exemplo, você pode determinar se o protetor de tela requer ou não uma senha. O WMI também oferece a capacidade de desligar um computador remoto.                                                                                                                                                               |
| [Discos e sistemas de arquivos](wmi-tasks--disks-and-file-systems.md)               | Obtenha informações sobre o estado de hardware da unidade de disco, volumes lógicos.                                                                                                                                                                                                                                                                                      |
| [Logs de eventos](wmi-tasks--event-logs.md)                                       | Obtenha dados de evento de arquivos de log de eventos do NT e execute operações como fazer o back-up ou limpar arquivos de log.                                                                                                                                                                                                                                                   |
| [Arquivos e pastas](wmi-tasks--files-and-folders.md)                         | Altere as propriedades de arquivo ou pasta por meio do WMI, incluindo a criação de um compartilhamento ou a renomeação de um arquivo.                                                                                                                                                                                                                                                              |
| [Rede](wmi-tasks--networking.md)                                       | Gerenciar e obter informações sobre conexões e endereços IP ou MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemas Operacionais](wmi-tasks--operating-systems.md)                         | Obtenha informações sobre o sistema operacional, como versão, se ele está ativado ou quais hotfixes estão instalados.                                                                                                                                                                                                                                  |
| [Monitoramento de desempenho](wmi-tasks--performance-monitoring.md)               | Use as classes WMI que obtém dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador.                                                                                                                                                                                                                                     |
| [Processos](wmi-tasks--processes.md)                                         | Obtenha informações como a conta na qual um processo está em execução. Você pode executar ações como a criação de processos.                                                                                                                                                                                                                                 |
| [Impressoras e impressão](wmi-tasks--printers-and-printing.md)                 | Gerencie e obtenha dados sobre impressoras, como localizar ou definir a impressora padrão.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Crie e modifique valores e chaves do Registro.                                                                                                                                                                                                                                                                                                               |
| [Tarefas agendadas](wmi-tasks--scheduled-tasks.md)                             | Criar e obter informações sobre tarefas agendadas.                                                                                                                                                                                                                                                                                                         |
| [Serviços](wmi-tasks--services.md)                                           | Obtenha informações sobre serviços, incluindo serviços dependentes ou antecessores.                                                                                                                                                                                                                                                                            |



 

 

 
