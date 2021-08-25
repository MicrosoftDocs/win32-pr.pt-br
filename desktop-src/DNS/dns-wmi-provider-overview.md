---
title: Visão geral do provedor WMI de DNS
description: um provedor é um elemento de arquitetura de Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Sistema de nomes de domínio, provedor WMI, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913156"
---
# <a name="dns-wmi-provider-overview"></a>Visão geral do provedor WMI de DNS

um provedor é um elemento de arquitetura de *Instrumentação de Gerenciamento do Windows (WMI)*. O WMI define uma arquitetura unificada para descrever, acessar e instrumentar objetos. Parte dessa arquitetura é um banco de dados grande de classes WMI usadas para realizar tarefas de gerenciamento remoto em objetos específicos.

Os provedores de WMI atuam como intermediários entre o WMI e um ou mais objetos gerenciados. Quando o WMI recebe uma solicitação de um aplicativo de gerenciamento para dados que não estão disponíveis no repositório CIM ou para notificações de eventos que o WMI não dá suporte, ele encaminha a solicitação para um provedor. Os provedores fornecem dados e notificações de eventos para os objetos gerenciados que são específicos para seus domínios. Um provedor estende o esquema WMI de classes para permitir que o WMI trabalhe com novos tipos de objetos. O provedor WMI de DNS define classes para consultar e configurar um servidor DNS, juntamente com suas zonas DNS e registros DNS associados.

O provedor WMI de DNS expõe vários objetos DNS para clientes, incluindo o servidor DNS, domínio DNS e objetos RR DNS. Por meio desses objetos, os clientes podem executar atividades de gerenciamento de DNS.

Usando o provedor WMI do DNS, você pode criar suas próprias ferramentas para executar a maioria das tarefas de administração do servidor DNS. Por exemplo, você pode criar, excluir e exibir zonas e registros; redefinir Propriedades de servidor e zona; e executar operações de administração rotineiras, como atualizar a zona, recarregar a zona, atualizar a zona, gravar a zona de volta em um arquivo ou Active Directory, pausar e retomar a zona, limpar o cache, parar e iniciar o serviço DNS e exibir estatísticas.

O provedor WMI de DNS tem um conjunto de comportamentos exclusivos não encontrado em outros provedores. Consulte a [referência do provedor WMI do DNS](dns-wmi-provider-reference.md) para obter detalhes da classe.

 

 




