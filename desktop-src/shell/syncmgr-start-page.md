---
description: O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador móvel ou um computador conectado a uma rede de área local.
title: gerenciador de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989009"
---
# <a name="synchronization-manager"></a>gerenciador de sincronização

## <a name="purpose"></a>Finalidade

O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador móvel ou um computador conectado a uma rede de área local. Junto com as funções de conectividade, as notificações (serviço de notificação de eventos do sistema) e o cache do lado do cliente, o Gerenciador de sincronização fornece uma infraestrutura para dar suporte à computação móvel. Em vez de cada aplicativo que implementa sua própria tecnologia para armazenar em cache e sincronizar recursos de rede para uso local, o sistema operacional fornece um modelo integrado que todos os aplicativos podem usar. Os arquivos são sincronizados independentemente do protocolo. Por exemplo, um programa de email pode transferir suas mensagens usando SMTP, NMTP ou POP3, enquanto um navegador pode usar HTTP e um banco de dados pode usar RPC (chamada de procedimento remoto). Os desenvolvedores podem usar a interface comum para o Gerenciador de sincronização em seus aplicativos para sincronizar arquivos entre o computador local do usuário e o armazenamento de rede.

## <a name="where-applicable"></a>Quando aplicável

O Gerenciador de sincronização destina-se a aplicativos que são executados principalmente em computadores móveis. Os aplicativos executados em computadores conectados a redes locais de alta latência também podem se beneficiar do uso do Gerenciador de sincronização.

## <a name="developer-audience"></a>Público de desenvolvedores

Este documento destina-se a desenvolvedores de software que desenvolvem aplicativos para computação móvel e redes locais de alta latência. Este documento fornece uma referência completa de todas as partes do Gerenciador de sincronização, incluindo os métodos e as interfaces para o Gerenciador de sincronização.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Requer o Windows Server 2003, o Windows XP, o Windows 2000 ou o Windows Millennium Edition (Windows me). Também disponível como um pacote redistribuível para Microsoft Windows NT 4,0, Windows 98 e Windows 95.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o Gerenciador de sincronização](syncmgr-about.md)<br/>                               | O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador local.<br/>     |
| [Configurações de computação móvel](syncmgr-mobile-computing-configs.md)<br/>          | Os aplicativos podem usar o sincronização Manager para manter arquivos e recursos armazenados em cache localmente e sincronizados em computadores móveis e de desktop.<br/> |
| [Cenários de aplicativos](syncmgr-app-scenarios.md)<br/>                               | Aplicativos e serviços que podem usar o Synchronization Manager.<br/>                                                                          |
| [Arquitetura do Gerenciador de sincronização](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Usando o Gerenciador de sincronização de um programa](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Referência do Synchronization Manager](syncmgr-reference.md)<br/>                       | Os seguintes elementos de programação compõem a API para o Gerenciador de sincronização.<br/>                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o serviço de notificação de eventos do sistema](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
