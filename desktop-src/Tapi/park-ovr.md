---
description: A operação de estacionamento permite que um aplicativo envie uma sessão para um endereço especial onde ele será mantido até que seja desestacionado.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Parque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779450"
---
# <a name="park"></a><span data-ttu-id="46bd6-103">Parque</span><span class="sxs-lookup"><span data-stu-id="46bd6-103">Park</span></span>

<span data-ttu-id="46bd6-104">A operação de estacionamento permite que um aplicativo envie uma sessão para um endereço especial onde ele será mantido até que seja desestacionado.</span><span class="sxs-lookup"><span data-stu-id="46bd6-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="46bd6-105">Do ponto de vista do aplicativo, isso é muito parecido com uma transferência.</span><span class="sxs-lookup"><span data-stu-id="46bd6-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="46bd6-106">Para a parte na outra extremidade da conexão, isso se parece ser colocado em espera.</span><span class="sxs-lookup"><span data-stu-id="46bd6-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="46bd6-107">A diferença entre o estacionamento e a transferência é que o endereço estacionado não é um ponto de conexão para a sessão, e a sessão não alerta ou atingiu o tempo limite. A diferença entre o estacionamento e o Hold é que, após a conclusão da operação de estacionamento, a sessão não estará mais associada ao endereço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46bd6-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="46bd6-108">São fornecidas duas formas de estacionamento de uma sessão: *Parque direcionado* e *estacionamento não direcionado*.</span><span class="sxs-lookup"><span data-stu-id="46bd6-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="46bd6-109">No parque de chamada direcionada, o aplicativo especifica o endereço de destino onde a chamada deve ser estacionada.</span><span class="sxs-lookup"><span data-stu-id="46bd6-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="46bd6-110">Com o estacionamento não direcionado, o provedor de serviços ou o hardware subjacente determina o endereço e o retorna para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46bd6-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="46bd6-111">Uma sessão estacionada normalmente entra no estado ocioso após ter sido estacionada com êxito e o aplicativo deve liberar os recursos associados a ele.</span><span class="sxs-lookup"><span data-stu-id="46bd6-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="46bd6-112">Consulte [encerrar uma sessão](terminate-a-session-ovr.md) para obter um resumo de como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="46bd6-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="46bd6-113">Se o aplicativo desestacionar a sessão, novos recursos de sessão serão alocados mesmo que o aplicativo tenha retornado os ponteiros anteriores, de modo que a falha de fazer as versões corretas pode resultar em uma variedade de problemas.</span><span class="sxs-lookup"><span data-stu-id="46bd6-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="46bd6-114">Alguns provedores de serviços podem lembrar o usuário após uma sessão ter sido estacionada por um longo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="46bd6-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="46bd6-115">O aplicativo vê uma chamada de oferta com um [motivo](reason-ovr.md) de chamada definido como lembrete.</span><span class="sxs-lookup"><span data-stu-id="46bd6-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="46bd6-116">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="46bd6-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="46bd6-117">**TAPI 2. x:** Consulte [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="46bd6-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="46bd6-118">**TAPI 3:** Consulte [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="46bd6-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
