---
description: A rede ATM (modo de transferência assíncrona) está surgindo na base da computação, e o suporte para ATM foi adicionado a muitas partes do sistema operacional.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualidade de serviço (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761227"
---
# <a name="quality-of-service-telephony-api"></a>Qualidade de serviço (API de telefonia)

A rede ATM (modo de transferência assíncrona) está surgindo na base da computação, e o suporte para ATM foi adicionado a muitas partes do sistema operacional. A TAPI também dá suporte a atributos-chave de estabelecimento de chamadas em instalações de ATM. O mais importante deles de uma perspectiva de aplicativo é a capacidade de solicitar, negociar, renegociar e receber indicações de parâmetros de qualidade de serviço (QOS) em chamadas de entrada e saída.

as informações de QOS na TAPI são trocadas entre aplicativos e provedores de serviço em estruturas [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) que são definidas no Windows sockets 2,0.

Os aplicativos solicitam QOS em chamadas de saída definindo valores de informações de sessão antes de iniciar uma sessão de comunicações. O provedor de serviços tentará fornecer a QOS especificada e a chamada será reprovada se não puder. O aplicativo pode então ajustar seus parâmetros e tentar a chamada novamente. Depois que uma chamada é estabelecida, um aplicativo pode solicitar uma alteração na QOS.

A TAPI fornece notificações de eventos para o proprietário ou monitorar aplicativos se houver qualquer alteração nos níveis de QOS.

O suporte para QOS não está restrito aos transportes ATM; qualquer provedor de serviços pode implementar recursos de QOS.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

* * TAPI 2. x: * *[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

* * TAPI 3. x: * *[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
