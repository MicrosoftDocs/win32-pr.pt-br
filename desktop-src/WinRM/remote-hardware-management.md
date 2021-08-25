---
title: Gerenciamento de hardware remoto
description: Gerenciamento de hardware remoto
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Gerenciamento de hardware remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db94c1f50b05f5180504ecef68bf10b1a5a596c9a9f88b96e7c5efb9faaa89bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858726"
---
# <a name="remote-hardware-management"></a>Gerenciamento de hardware remoto

Windows O gerenciamento remoto de hardware é destinado a reduzir os custos gerais de administração de ti, fornecendo monitoramento e controle de componentes de hardware remotos, especialmente antes de o sistema ser iniciado e após uma falha do sistema operacional.

Os OEMs (fabricantes originais de equipamento) desenvolveram uma arquitetura comum para atender à necessidade de gerenciamento de hardware. Uma parte importante dessa arquitetura é o [*Baseboard Management Controller*](windows-remote-management-glossary.md) (BMC). Um BMC é um dispositivo especializado que monitora o estado do computador do servidor. O BMC fornece controle remoto de hardware de servidor, recupera dados de status e recebe notificações sobre erros críticos e outras alterações de status de hardware. Um script ou aplicativo que está monitorando um servidor remoto pode obter dados do servidor [*em banda*](windows-remote-management-glossary.md), por meio do sistema operacional remoto, ou [*fora de banda*](windows-remote-management-glossary.md), diretamente do BMC.

Um BMC tem sensores que podem detectar, por exemplo, quando o computador do servidor está superaquecendo ou quando a tensão está fora do intervalo aceitável. Existem vários padrões para definir a arquitetura do BMC. A [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md) é um padrão que é usado com frequência. No entanto, apesar do padrão IPMI, o acesso de gerenciamento ao hardware do servidor é proprietário e requer o uso de ferramentas de gerenciamento fornecidas pelos OEMs. Além disso, o acesso remoto a um BMC é fornecido usando um protocolo de fio especializado, o protocolo de controle de gerenciamento remoto (RMCP), que tem mecanismos de segurança não padrão para autenticação de acesso.

O [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) da Microsoft e o driver IPMI permitem obter dados do BMC de computadores de servidor remoto por meio de um provedor WMI padrão com [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI. Embora você possa escrever um script WMI normal que obtenha dados remotos por meio do DCOM, em muitos casos, o método preferencial de obtenção de dados do IPMI é por meio do utilitário de linha de comando **WinRM** ou da API de [script](winrm-scripting-api.md) do WinRM ou da [API C++ do WinRM](winrm-c---api.md). O utilitário WinRM e as APIs do serviço WinRM dependem do protocolo WS-Management e podem obter dados de IPMI de um computador local ou remoto sem usar o DCOM.

O BMC também tem um banco de dados de eventos chamado de SEL (log de eventos do sistema) que registra os eventos no computador monitorado. Você não pode se inscrever para ter esses eventos entregues a um script como é possível com as classes de evento WMI. No entanto, você pode usar a ferramenta de linha de comando Wecutil.exe para assiná-las. Para obter mais informações sobre como usar essa ferramenta, em um prompt de comando, digite **wecutil/?**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> <dt>

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> </dl>

 

 