---
description: A rede do ATM (Modo de Transferência Assíncrona) está emergente na base da computação e o suporte para ATM foi adicionado a muitas partes do sistema operacional.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualidade de serviço (API de Telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761227"
---
# <a name="quality-of-service-telephony-api"></a>Qualidade de serviço (API de Telefonia)

A rede do ATM (Modo de Transferência Assíncrona) está emergente na base da computação e o suporte para ATM foi adicionado a muitas partes do sistema operacional. A TAPI também dá suporte a atributos principais do estabelecimento de chamadas em instalações do ATM. O mais importante deles de uma perspectiva de aplicativo é a capacidade de solicitar, negociar, negociar e receber indicações de parâmetros QOS (Qualidade de Serviço) em chamadas de entrada e saída.

As informações do QOS na TAPI são trocadas entre aplicativos e provedores de serviços em estruturas [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definidas no Windows Sockets 2.0.

Os aplicativos solicitam qOS em chamadas de saída definindo valores de informações de sessão antes de iniciar uma sessão de comunicação. O provedor de serviços tentará fornecer o QOS especificado e falhará na chamada se não puder. Em seguida, o aplicativo pode ajustar seus parâmetros e tentar a chamada novamente. Depois que uma chamada é estabelecida, um aplicativo pode solicitar uma alteração no QOS.

A TAPI fornece notificações de eventos para o proprietário ou monitorar aplicativos se houver qualquer alteração nos níveis de QOS.

O suporte para QOS não está restrito a transporte de atm; qualquer provedor de serviços pode implementar recursos do QOS.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x: **[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

**TAPI 3.x: **[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
