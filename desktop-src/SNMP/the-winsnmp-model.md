---
title: O modelo WinSNMP
description: O modelo compatível com WinSNMP inclui os componentes básicos a seguir.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127576"
---
# <a name="the-winsnmp-model"></a>O modelo WinSNMP

O modelo compatível com WinSNMP inclui os seguintes componentes básicos:

-   Um aplicativo de gerenciamento de rede SNMP habilitado para WinSNMP, ou seja, um *aplicativo* compatível com WinSNMP
-   A camada de função WinSNMP
-   Um provedor de serviços SNMP habilitado para WinSNMP, ou seja, uma *implementação* compatível com o WinSNMP

Os aplicativos de gerenciamento de rede que devem transmitir mensagens SNMP operam com eficiência em um ambiente orientado a eventos. Isso ocorre porque o SNMP é um protocolo baseado em datagrama ou sem conexão entre entidades remotas que não estabelecem circuitos virtuais.

como os aplicativos Microsoft Windows também são controlados por evento, o WinSNMP usa um modelo de programação no qual o recebimento e o processamento de *eventos de mensagens* assíncronas orientam os aplicativos de gerenciamento. Um evento de mensagem assíncrona pode ser uma solicitação de operação SNMP por um aplicativo de gerente ou a resposta a uma solicitação por um aplicativo do Agent.

SNMP envia solicitações e respostas como mensagens SNMP. Uma mensagem SNMP é uma PDU (unidade de dados de protocolo SNMP) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante. Para obter mais informações, consulte [sobre mensagens SNMP](about-snmp-messages.md), [trabalhando com listas de associação de variáveis](working-with-variable-binding-lists.md) e [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).

 

 




