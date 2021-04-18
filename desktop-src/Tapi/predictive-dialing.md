---
description: A discagem preditiva é um aplicativo que normalmente é executado em um servidor de telefonia do Call Center.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Discagem preditiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783353"
---
# <a name="predictive-dialing"></a>Discagem preditiva

A discagem preditiva é um aplicativo que normalmente é executado em um servidor de telefonia do Call Center. Ele usa uma lista de números de telefone, geralmente obtidos de um banco de dados, para tentar chamadas de saída; Quando uma chamada é *concluída*, a chamada é automaticamente atribuída a um agente para manipulação. O aplicativo pode fazer uso de uma *porta de discagem preditiva* em um comutador, que é um dispositivo que pode fazer chamadas de saída e tem capacidades especiais (por meio do DSP e assim por diante) para detectar tons de progresso de chamada e outras indicações audíveis de estado de chamada. Quando uma chamada é feita em uma porta de discagem preditiva, normalmente ela é automaticamente transferida para outro dispositivo no comutador quando a chamada atinge um estado específico ou após a detecção de um tipo de mídia específico; Esse dispositivo de destino pode ser uma fila para agentes que manipulam chamadas de saída.

Os aplicativos identificam um dispositivo como tendo capacidade de discagem preditiva pelo LINEADDRCAPFLAGS \_ PREDICTIVEDIALER bit no membro **DwAddrCapFlags** no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). O membro **dwPredictiveAutoTransferStates** em **LINEADDRESSCAPS** indica os Estados nos quais a porta de discagem preditiva pode ser acionada para transferir automaticamente uma chamada; Se esse membro for zero, ele indicará que a transferência automática não está disponível e que é responsabilidade do aplicativo de transferir chamadas explicitamente ao detectar o estado de chamada apropriado (ou tipo de mídia ou outros critérios). Preferencialmente, os fabricantes de comutador disponibilizarão a transferência automática e manual e permitirão que os aplicativos selecionem o mecanismo preferencial, mas os provedores de serviço precisarão modelar o comportamento do equipamento herdado. Uma única porta de discagem preditiva (endereço/dispositivo de linha) pode dar suporte à realização de várias chamadas de saída simultaneamente, conforme indicado pelo membro **dwMaxNumActiveCalls** em **LINEADDRESSCAPS**. O recurso de discagem preditiva também pode ser disponibilizado em qualquer dispositivo, usando um pool compartilhado de processadores de sinal de discagem preditiva, que são ligados na linha que está sendo conectada mediante solicitação.

Quando a função [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) é usada em uma linha capaz de discagem preditiva (uma porta com o \_ conjunto PREDICTIVEDIALER LINEADDRCAPFLAGS) e a discagem preditiva é solicitada usando LINECALLPARAMFLAGS \_ PREDICTIVEDIAL, a chamada é feita de forma preditiva com a detecção de progresso de chamada audível avançada. Campos e constantes adicionais são definidos na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passada para **lineMakeCall** para controlar o comportamento da porta de discagem preditiva. O membro **dwPredictiveAutoTransferStates** indica que a chamada de linha declara que, na entrada da chamada em qualquer uma delas, a porta de discagem preditiva deve transferir automaticamente a chamada para o destino designado (os bits devem ser um subconjunto adequado dos Estados de transferência automática com suporte indicados no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); o aplicativo pode deixar o campo definido como 0 se desejar monitorar os próprios Estados de chamada e usar [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) para transferir a chamada quando ela atingir a condição desejada. O aplicativo deve especificar o endereço desejado para o qual a chamada deve ser automaticamente transferida no campo de variável definido pelos membros **dwTargetAddressSize** e **dwTargetAddressOffset** em **LINECALLPARAMS**.

Os aplicativos também podem definir um tempo limite para chamadas de saída para que o provedor de serviços as migre automaticamente para um estado desconectado se não forem respondidas. Isso é controlado usando o membro **dwNoAnswerTimeout** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



