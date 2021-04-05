---
title: Cancelando a retransmissão
description: Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões forem especificadas para a entidade, a implementação do Microsoft WinSNMP retransmitirá a solicitação.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005512"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="88df5-103">Cancelando a retransmissão</span><span class="sxs-lookup"><span data-stu-id="88df5-103">Canceling Retransmission</span></span>

<span data-ttu-id="88df5-104">Se não houver resposta a uma solicitação de comunicação dentro do período de tempo limite especificado para uma entidade de destino e se as retransmissões forem especificadas para a entidade, a implementação do Microsoft WinSNMP retransmitirá a solicitação.</span><span class="sxs-lookup"><span data-stu-id="88df5-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="88df5-105">Uma chamada para a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) pode cancelar esse ciclo de retransmissão e liberar estruturas de dados internas associadas à solicitação de mensagem.</span><span class="sxs-lookup"><span data-stu-id="88df5-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="88df5-106">Observe que é possível que uma entidade de destino receba uma mensagem SNMP que foi cancelada por uma chamada para a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) .</span><span class="sxs-lookup"><span data-stu-id="88df5-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="88df5-107">Também é possível que uma entidade de destino possa responder a uma mensagem SNMP cancelada.</span><span class="sxs-lookup"><span data-stu-id="88df5-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="88df5-108">Isso acontece porque o serviço de enfileiramento de transações ocorre em vários níveis.</span><span class="sxs-lookup"><span data-stu-id="88df5-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="88df5-109">No entanto, depois que uma mensagem for cancelada por uma chamada para [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), a implementação do Microsoft WinSNMP não retransmitirá a mensagem, enviará uma PDU de resposta ou enviará uma notificação de tempo limite para o aplicativo para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="88df5-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 




