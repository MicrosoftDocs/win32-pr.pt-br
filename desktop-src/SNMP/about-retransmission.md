---
title: Sobre a retransmissão
description: Um aplicativo WinSNMP pode fazer solicitações de operação SNMP de várias maneiras.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291968"
---
# <a name="about-retransmission"></a><span data-ttu-id="4ebeb-103">Sobre a retransmissão</span><span class="sxs-lookup"><span data-stu-id="4ebeb-103">About Retransmission</span></span>

<span data-ttu-id="4ebeb-104">Um aplicativo WinSNMP pode fazer solicitações de operação SNMP de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-104">A WinSNMP application can make SNMP operation requests in various ways.</span></span> <span data-ttu-id="4ebeb-105">O aplicativo pode emitir várias solicitações para um agente SNMP, sem aguardar uma resposta, ou pode emitir uma única solicitação e aguardar a resposta.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-105">The application can issue several requests to an SNMP agent, without waiting for a response, or it can issue a single request and wait for the response.</span></span> <span data-ttu-id="4ebeb-106">Como o SNMP pode ser implementado em vários protocolos de transporte, os mecanismos de entrega e as características de confiabilidade podem variar.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-106">Since SNMP can be implemented on multiple transport protocols, delivery mechanisms and reliability characteristics can vary.</span></span>

<span data-ttu-id="4ebeb-107">Ao codificar o aplicativo WinSNMP, você deve determinar o nível de confiabilidade de que precisa para operações de comunicação, com base na maneira como o aplicativo emite solicitações de operação.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-107">When you code the WinSNMP application you must determine the level of reliability you need for communications operations, based on the way the application issues operation requests.</span></span> <span data-ttu-id="4ebeb-108">Em seguida, você deve selecionar uma estratégia de retransmissão e implementar uma política de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-108">Then you must select a retransmission strategy and implement a retransmission policy.</span></span>

<span data-ttu-id="4ebeb-109">Uma política de retransmissão inclui um período de tempo limite e uma contagem de repetição.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-109">A retransmission policy includes a time-out period and a retry count.</span></span> <span data-ttu-id="4ebeb-110">Um período de tempo limite é o tempo decorrido, em centésimos de segundo, entre a emissão de um aplicativo de uma solicitação [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e seu recebimento da mensagem correspondente.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-110">A time-out period is the elapsed time, in hundredths of a second, between an application's issuance of an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request and its receipt of the corresponding message.</span></span> <span data-ttu-id="4ebeb-111">O aplicativo recebe a mensagem como resultado de uma chamada para a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="4ebeb-111">The application receives the message as a result of a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function.</span></span> <span data-ttu-id="4ebeb-112">O valor de tempo limite é o período de tempo durante o qual a implementação do Microsoft WinSNMP aguarda uma entidade responder a uma solicitação de comunicação.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-112">The time-out value is the period of time the Microsoft WinSNMP implementation waits for an entity to respond to a communication request.</span></span> <span data-ttu-id="4ebeb-113">Se não houver resposta dentro do período de tempo limite, a implementação retransmitirá a solicitação se o valor de contagem de repetição especificar tentativas de retransmissão ou falhar na chamada para [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="4ebeb-113">If there is no response within the time-out period, the implementation either retransmits the request if the retry count value specifies retransmission attempts, or it fails the call to [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span> <span data-ttu-id="4ebeb-114">Uma contagem de repetição é o número máximo de tentativas de retransmissão que a implementação faz se uma solicitação de transmissão SNMP falhar.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-114">A retry count is the maximum number of retransmission attempts the implementation makes if an SNMP transmission request fails.</span></span>

<span data-ttu-id="4ebeb-115">A implementação armazena valores de tempo limite e contagens de repetição em seu banco de dados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-115">The implementation stores time-out values and retry counts in its database for the application.</span></span> <span data-ttu-id="4ebeb-116">A implementação armazena valores individuais para cada entidade de destino.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-116">The implementation stores individual values for each destination entity.</span></span>

<span data-ttu-id="4ebeb-117">Os aplicativos devem estabelecer suas próprias frequências de sondagem e devem gerenciar variáveis de temporizador.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-117">Applications must establish their own polling frequencies and they must manage timer variables.</span></span> <span data-ttu-id="4ebeb-118">Para obter mais informações, consulte [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="4ebeb-118">For more information, see [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




