---
title: Atribuindo identificadores de solicitação
description: Um aplicativo WinSNMP pode chamar a função SnmpCreatePdu ou a função SnmpSetPduData para atribuir um identificador de solicitação gerado pelo aplicativo a um PDU. O aplicativo deve passar o valor no \_ parâmetro ID da solicitação.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634841"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="d40f2-104">Atribuindo identificadores de solicitação</span><span class="sxs-lookup"><span data-stu-id="d40f2-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="d40f2-105">Um aplicativo WinSNMP pode chamar a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) para atribuir um identificador de solicitação gerado pelo aplicativo a um PDU.</span><span class="sxs-lookup"><span data-stu-id="d40f2-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="d40f2-106">O aplicativo deve passar o valor no parâmetro *\_ ID da solicitação* .</span><span class="sxs-lookup"><span data-stu-id="d40f2-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="d40f2-107">Um aplicativo pode solicitar que a implementação do Microsoft WinSNMP gere e atribua um identificador de solicitação a um PDU passando zero no *parâmetro \_ ID da solicitação* da função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="d40f2-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="d40f2-108">O aplicativo pode recuperar o identificador de solicitação atribuído com uma chamada para a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="d40f2-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="d40f2-109">Para atribuir um identificador de solicitação igual a um valor específico, incluindo zero, o aplicativo deve passar esse valor no *parâmetro \_ ID da solicitação* da função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="d40f2-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="d40f2-110">Quando a implementação executa a política de retransmissão do aplicativo, ela inclui o **campo \_ ID da solicitação** do PDU original em cada mensagem SNMP retransmitida.</span><span class="sxs-lookup"><span data-stu-id="d40f2-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="d40f2-111">Para obter mais informações, consulte [sobre a retransmissão](about-retransmission.md) e [Gerenciamento da política de retransmissão](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="d40f2-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="d40f2-112">Quando a implementação recebe interceptações de uma entidade SNMPv1, ela atribui um valor diferente de zero ao campo **\_ ID da solicitação** da PDU.</span><span class="sxs-lookup"><span data-stu-id="d40f2-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="d40f2-113">Esse valor pode duplicar um identificador de solicitação usado pelo aplicativo em uma PDU de solicitação.</span><span class="sxs-lookup"><span data-stu-id="d40f2-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="d40f2-114">Os aplicativos devem verificar a duplicação.</span><span class="sxs-lookup"><span data-stu-id="d40f2-114">Applications must check for duplication.</span></span>

 

 

 




