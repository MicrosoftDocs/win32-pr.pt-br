---
title: O banco de dados WinSNMP
description: A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f478c9bb1c05d3a094e2a15fac0a9cef5968f245257a0702d045eb90bd2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885996"
---
# <a name="the-winsnmp-database"></a>O banco de dados WinSNMP

A implementação do Microsoft WinSNMP mantém um armazenamento de informações administrativas em um banco de dados. O banco de dados inclui as seguintes informações:

-   Propriedades de rede e versão.

    A implementação usa essas propriedades para determinar qual protocolo de transporte de rede e a estrutura de versão SNMP usar para concluir solicitações de transmissão. Para obter mais informações, consulte [sobre as versões SNMP](about-snmp-versions.md).

-   Modo de tradução de contexto e entidade.

    A implementação usa esse modo para interpretar nomes amigáveis para entidades e contextos SNMP. Para obter mais informações, consulte [definindo a entidade e o modo de tradução de contexto](setting-the-entity-and-context-translation-mode.md).

-   Configuração de política de retransmissão.

    A implementação usa essa configuração para determinar se ela deve ou não executar a política de retransmissão do aplicativo. A implementação armazena um valor de tempo limite e uma contagem de repetição para cada entidade de destino. Para obter mais informações, consulte [sobre a retransmissão](about-retransmission.md) e [Gerenciamento da política de retransmissão](managing-the-retransmission-policy.md).

 

 




