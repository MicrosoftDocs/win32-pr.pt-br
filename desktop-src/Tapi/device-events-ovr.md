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
# <a name="device-events-telephony-api"></a><span data-ttu-id="1f6f3-103">Eventos de dispositivo (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="1f6f3-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="1f6f3-104">A TAPI responde às alterações do dispositivo, como um telefone que começou a tocar ou um modem que foi removido por meio do acionamento de eventos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="1f6f3-105">Um aplicativo TAPI deve responder a um evento de dispositivo consultando a alteração específica que ocorreu e, em seguida, executando a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="1f6f3-106">Um aplicativo pode exibir eventos que receberá usando a [notificação de eventos](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1f6f3-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="1f6f3-107">**TAPI 2. x:** Os aplicativos recebem a notificação de eventos de dispositivo usando a [**linha \_ LINEDEVSTATE**](./line-linedevstate.md) Message.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="1f6f3-108">O status atual de um endereço é determinado pela chamada de [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), que retorna suas informações em uma estrutura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="1f6f3-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="1f6f3-109">O status de um dispositivo de linha aberta especificado é obtido chamando [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), que retorna suas informações em uma estrutura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="1f6f3-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="1f6f3-110">**TAPI 3. x:** Os aplicativos recebem uma notificação de [**\_ evento de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , que é processada usando a interface [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) .</span><span class="sxs-lookup"><span data-stu-id="1f6f3-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="1f6f3-111">O [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) pode então ser usado para adquirir informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="1f6f3-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
