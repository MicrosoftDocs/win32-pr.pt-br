---
title: O banco de dados WinSNMP
description: A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453559"
---
# <a name="the-winsnmp-database"></a>O banco de dados WinSNMP

A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados. O banco de dados inclui as seguintes informações:

-   Propriedades de rede e versão.

    A implementação usa essas propriedades para determinar qual protocolo de transporte de rede e a estrutura de versão SNMP usar para concluir solicitações de transmissão. Para obter mais informações, consulte [sobre as versões SNMP](about-snmp-versions.md).

-   Modo de tradução de contexto e entidade.

    A implementação usa esse modo para interpretar nomes amigáveis para entidades e contextos SNMP. Para obter mais informações, consulte [definindo a entidade e o modo de tradução de contexto](setting-the-entity-and-context-translation-mode.md).

-   Configuração de política de retransmissão.

    A implementação usa essa configuração para determinar se ela deve ou não executar a política de retransmissão do aplicativo. A implementação armazena um valor de tempo limite e uma contagem de repetição para cada entidade de destino. Para obter mais informações, consulte [sobre a retransmissão](about-retransmission.md) e [Gerenciamento da política de retransmissão](managing-the-retransmission-policy.md).

 

 




