---
title: Sobre SNMP
description: O SNMP usa uma arquitetura distribuída que consiste em gerentes e agentes.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007992"
---
# <a name="about-snmp"></a>Sobre SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

O SNMP usa uma arquitetura distribuída que consiste em gerentes e agentes. Um agente é um aplicativo SNMP que responde a consultas de aplicativos do Gerenciador SNMP. O agente SNMP é responsável por recuperar e atualizar informações de gerenciamento local com base nas solicitações do Gerenciador SNMP. O agente também notifica os gerentes registrados quando ocorrem eventos ou interceptações significativos. Um gerente é um aplicativo SNMP que gera consultas para aplicativos de agente SNMP e recebe interceptações de aplicativos de agente SNMP.

Em computadores que executam o Microsoft Windows XP/Windows 2000/Windows NT, o agente SNMP é implementado pelo serviço SNMP (SNMP.EXE). O Gerenciador SNMP normalmente é um aplicativo de console de gerenciamento SNMP de terceiros. O aplicativo de console de gerenciamento não precisa ser executado no mesmo host que o agente SNMP. Para usar as informações fornecidas pelo serviço SNMP da Microsoft, você precisa de pelo menos um aplicativo de console de gerenciamento SNMP. O sistema inclui bibliotecas que dão suporte a aplicativos de console de gerenciamento SNMP, mas não inclui um aplicativo de console de gerenciamento SNMP no momento.

 

 