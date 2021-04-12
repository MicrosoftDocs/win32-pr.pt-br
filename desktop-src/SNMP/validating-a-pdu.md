---
title: Validando uma PDU
description: Quando o aplicativo WinSNMP chama a função SnmpSendMsg ou a função SnmpEncodeMsg, a implementação do Microsoft WinSNMP verifica a validade da PDU e os outros parâmetros de função.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364278"
---
# <a name="validating-a-pdu"></a><span data-ttu-id="5e8a1-103">Validando uma PDU</span><span class="sxs-lookup"><span data-stu-id="5e8a1-103">Validating a PDU</span></span>

<span data-ttu-id="5e8a1-104">Quando o aplicativo WinSNMP chama a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , a implementação do Microsoft WinSNMP verifica a validade da PDU e os outros parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-104">When the WinSNMP application calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function, the Microsoft WinSNMP implementation verifies the validity of the PDU and the other function parameters.</span></span>

<span data-ttu-id="5e8a1-105">O valor de um componente de dados PDU (ou campo) pode ser válido individualmente, mas pode ser inválido em combinação com valores para outros campos.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-105">The value of one PDU data component (or field) can be valid individually, but it may be invalid in combination with values for other fields.</span></span> <span data-ttu-id="5e8a1-106">Por exemplo, a menos que o campo de **\_ tipo de PDU** da PDU seja uma resposta de PDU do SNMP \_ PDU \_ GetBulk ou SNMP \_ , os \_ campos **\_ status de erro** e **\_ índice de erro** devem ser iguais a zero.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-106">For example, unless the **PDU\_type** field of the PDU is SNMP\_PDU\_GETBULK or SNMP\_PDU\_RESPONSE, both the **error\_status** and **error\_index** fields must be equal to zero.</span></span> <span data-ttu-id="5e8a1-107">Qualquer outra combinação de valor constitui um PDU inválido.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-107">Any other value combination constitutes an invalid PDU.</span></span>

<span data-ttu-id="5e8a1-108">A implementação rejeita PDUs inválidas e retorna o status de erro SNMPAPI \_ falha.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-108">The implementation rejects invalid PDUs and returns the error status SNMPAPI\_FAILURE.</span></span> <span data-ttu-id="5e8a1-109">Ele define um código de erro estendido igual a SNMPAPI \_ PDU \_ inválido.</span><span class="sxs-lookup"><span data-stu-id="5e8a1-109">It sets an extended error code equal to SNMPAPI\_PDU\_INVALID.</span></span>

 

 




