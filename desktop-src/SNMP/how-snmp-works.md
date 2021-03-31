---
title: Como funciona o SNMP
description: Como um aplicativo de console de gerenciamento SNMP de terceiros retorna informações do serviço SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916131"
---
# <a name="how-snmp-works"></a>Como funciona o SNMP

As etapas a seguir descrevem como um aplicativo de console de gerenciamento SNMP de terceiros retorna informações do serviço SNMP:

1.  O aplicativo de console de gerenciamento SNMP formula uma mensagem SNMP com base na entrada do usuário. A mensagem inclui uma PDU (unidade de dados de protocolo) e informações de autenticação. O aplicativo de console de gerenciamento pode usar a biblioteca de API de gerenciamento SNMP da Microsoft (MGMTAPI.DLL) ou a biblioteca de API do Microsoft [WinSNMP](winsnmp-api.md) (WSNMP32.DLL) para executar essa etapa.
2.  O aplicativo de console de gerenciamento SNMP envia a mensagem SNMP para o serviço SNMP, usando as bibliotecas de serviço SNMP.
3.  O serviço SNMP recebe a solicitação. Ele verifica as informações de autenticação e o endereço IP de origem.
4.  O serviço SNMP seleciona o agente de extensão apropriado e solicita que o agente recupere as informações solicitadas.
5.  O serviço SNMP envia a resposta para o aplicativo de console de gerenciamento SNMP.

 

 




