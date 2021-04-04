---
description: A TAPI responde às alterações do dispositivo, como um telefone que começou a tocar ou um modem que foi removido por meio do acionamento de eventos do dispositivo.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Eventos de dispositivo (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647181"
---
# <a name="device-events-telephony-api"></a>Eventos de dispositivo (API de telefonia)

A TAPI responde às alterações do dispositivo, como um telefone que começou a tocar ou um modem que foi removido por meio do acionamento de eventos do dispositivo. Um aplicativo TAPI deve responder a um evento de dispositivo consultando a alteração específica que ocorreu e, em seguida, executando a ação apropriada. Um aplicativo pode exibir eventos que receberá usando a [notificação de eventos](event-notification.md).

**TAPI 2. x:** Os aplicativos recebem a notificação de eventos de dispositivo usando a [**linha \_ LINEDEVSTATE**](./line-linedevstate.md) Message. O status atual de um endereço é determinado pela chamada de [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), que retorna suas informações em uma estrutura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) . O status de um dispositivo de linha aberta especificado é obtido chamando [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), que retorna suas informações em uma estrutura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .

**TAPI 3. x:** Os aplicativos recebem uma notificação de [**\_ evento de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , que é processada usando a interface [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) . O [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) pode então ser usado para adquirir informações mais detalhadas.

 

 
