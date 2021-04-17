---
description: Tanto os provedores de C++ quanto os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protegendo clientes e provedores do C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782542"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="cb712-103">Protegendo clientes e provedores do C++</span><span class="sxs-lookup"><span data-stu-id="cb712-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="cb712-104">Tanto os provedores de C++ quanto os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.</span><span class="sxs-lookup"><span data-stu-id="cb712-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="cb712-105">Os aplicativos cliente devem definir a [representação](setting-the-default-process-security-level-using-c-.md) DCOM e os níveis de [autenticação](setting-authentication-in-wmi.md) corretamente ao se conectar ao WMI.</span><span class="sxs-lookup"><span data-stu-id="cb712-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="cb712-106">Os retornos de chamada de [chamadas assíncronas](setting-security-on-an-asynchronous-call.md) têm riscos de segurança, portanto, os aplicativos cliente devem [executar verificações de acesso](performing-access-checks.md) para garantir que o retorno de chamada seja de uma fonte confiável.</span><span class="sxs-lookup"><span data-stu-id="cb712-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="cb712-107">Os clientes precisam proteger os [consumidores de eventos temporários e permanentes](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="cb712-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="cb712-108">Um provedor pode [executar verificações de acesso](performing-access-checks.md) para garantir que os recursos que ele cria sejam acessados somente por clientes apropriados.</span><span class="sxs-lookup"><span data-stu-id="cb712-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="cb712-109">Os provedores e os clientes também podem definir a segurança em uma conexão de [proxy específica](setting-the-security-on-iwbemservices-and-other-proxies.md) .</span><span class="sxs-lookup"><span data-stu-id="cb712-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="cb712-110">Ambos também podem habilitar [privilégios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="cb712-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="cb712-111">Um provedor de eventos deve garantir que o consumidor do cliente tenha privilégios para [receber um evento solicitado](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="cb712-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="cb712-112">Um cliente ou provedor pode precisar fazer uma conexão remota que exige um serviço de autenticação diferente, NTLM em vez de Kerberos, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="cb712-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



