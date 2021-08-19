---
description: A discagem preditiva é um aplicativo que normalmente é executado em um servidor de telefonia do call center.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Discagem preditiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d930a0a49751c7f1851600e277d2cf201f0acbe1a9da3f7be5aa9f2e4b38439c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060594"
---
# <a name="predictive-dialing"></a>Discagem preditiva

A discagem preditiva é um aplicativo que normalmente é executado em um servidor de telefonia do call center. Ele usa uma lista de números de telefone, geralmente obtidos de um banco de dados, para tentar chamadas de saída; quando uma chamada é *concluída*, a chamada é atribuída automaticamente a um agente para manipulação. O aplicativo pode usar  uma porta de discagem preditiva em um comutamento, que é um dispositivo que pode fazer chamadas de saída e tem habilidades especiais (por meio do DSP e assim por diante) para detectar tons de progresso da chamada e outras indicações audíveis de estado de chamada. Quando uma chamada é feita em uma porta de discagem preditiva, normalmente ela é transferida automaticamente para outro dispositivo na opção quando a chamada atinge um estado específico ou após a detecção de um tipo de mídia específico; esse dispositivo de destino pode ser uma fila para agentes que manipulam chamadas de saída.

Os aplicativos identificam um dispositivo como tendo a capacidade de discagem preditiva pelo bit PREDICTIVEDIALER LINEADDRCAPFLAGS no membro \_ **dwAddrCapFlags** [**em LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). O **membro dwPredictiveAutoTransferStates** em **LINEADDRESSCAPS** indica os estados nos quais a porta de discagem preditiva pode ser comandoada para transferir automaticamente uma chamada; se esse membro for zero, isso indicará que a transferência automática não está disponível e que é responsabilidade do aplicativo transferir chamadas explicitamente após detectar o estado de chamada apropriado (ou o tipo de mídia ou outros critérios). Preferencialmente, os fabricantes de comutdores disponibilizam a transferência automática e manual e permitem que os aplicativos selecionem o mecanismo preferencial, mas os provedores de serviços teriam que modelar o comportamento do equipamento herdado. Uma única porta de discagem preditiva (dispositivo/endereço de linha) pode dar suporte à tomada de várias chamadas de saída simultaneamente, conforme indicado pelo membro **dwMaxNumActiveCalls** em **LINEADDRESSCAPS**. A funcionalidade de discagem preditiva também pode ser disponibilizada em qualquer dispositivo, usando um pool compartilhado de processadores de sinal de discagem preditiva, que são conectados à linha que está sendo discada mediante solicitação.

Quando a função [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) é usada em uma linha capaz de discagem preditiva (uma porta com o conjunto LINEADDRCAPFLAGS PREDICTIVEDIALER) e a discagem preditiva é solicitada usando \_ LINECALLPARAMFLAGS PREDICTIVEDIAL, a chamada é feita de forma preditiva com detecção de progresso de chamada aprimorada. \_ Campos e constantes adicionais são definidos na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passada para **lineMakeCall** para controlar o comportamento da porta de discagem preditiva. O membro **dwPredictiveAutoTransferStates** indica que, após a entrada da chamada em qualquer um deles, a porta de discagem preditiva deve transferir automaticamente a chamada para o destino designado (os bits devem ser um subconjunto adequado dos estados de transferência automática com suporte indicados em [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); O aplicativo poderá deixar o campo definido como 0 se desejar monitorar os próprios estados de chamada e usar [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) para transferir a chamada quando atingir a condição desejada. O aplicativo deve especificar o endereço desejado para o qual a chamada deve ser transferida automaticamente no campo variável definido pelos membros **dwTargetAddressSize** e **dwTargetAddressOffset** em **LINECALLPARAMS**.

Os aplicativos também podem definir um tempo de saída para chamadas de saída para que o provedor de serviços as transições automáticas para um estado desconectado se elas não são respondidas. Isso é controlado usando **o membro dwNoAnswerTimeout** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



