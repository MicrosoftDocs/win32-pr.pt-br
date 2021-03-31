---
description: A rede ATM (modo de transferência assíncrona) está surgindo na base da computação, e o suporte para ATM foi adicionado a muitas partes do sistema operacional.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualidade de serviço (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829514"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="92e1e-103">Qualidade de serviço (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="92e1e-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="92e1e-104">A rede ATM (modo de transferência assíncrona) está surgindo na base da computação, e o suporte para ATM foi adicionado a muitas partes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="92e1e-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="92e1e-105">A TAPI também dá suporte a atributos-chave de estabelecimento de chamadas em instalações de ATM.</span><span class="sxs-lookup"><span data-stu-id="92e1e-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="92e1e-106">O mais importante deles de uma perspectiva de aplicativo é a capacidade de solicitar, negociar, renegociar e receber indicações de parâmetros de qualidade de serviço (QOS) em chamadas de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="92e1e-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="92e1e-107">As informações de QOS na TAPI são trocadas entre aplicativos e provedores de serviço em estruturas [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) que são definidas no Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="92e1e-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="92e1e-108">Os aplicativos solicitam QOS em chamadas de saída definindo valores de informações de sessão antes de iniciar uma sessão de comunicações.</span><span class="sxs-lookup"><span data-stu-id="92e1e-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="92e1e-109">O provedor de serviços tentará fornecer a QOS especificada e a chamada será reprovada se não puder.</span><span class="sxs-lookup"><span data-stu-id="92e1e-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="92e1e-110">O aplicativo pode então ajustar seus parâmetros e tentar a chamada novamente.</span><span class="sxs-lookup"><span data-stu-id="92e1e-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="92e1e-111">Depois que uma chamada é estabelecida, um aplicativo pode solicitar uma alteração na QOS.</span><span class="sxs-lookup"><span data-stu-id="92e1e-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="92e1e-112">A TAPI fornece notificações de eventos para o proprietário ou monitorar aplicativos se houver qualquer alteração nos níveis de QOS.</span><span class="sxs-lookup"><span data-stu-id="92e1e-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="92e1e-113">O suporte para QOS não está restrito aos transportes ATM; qualquer provedor de serviços pode implementar recursos de QOS.</span><span class="sxs-lookup"><span data-stu-id="92e1e-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="92e1e-114">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="92e1e-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="92e1e-115">\* \* TAPI 2. x: \* \*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="92e1e-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="92e1e-116">\* \* TAPI 3. x: \* \*[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="92e1e-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
