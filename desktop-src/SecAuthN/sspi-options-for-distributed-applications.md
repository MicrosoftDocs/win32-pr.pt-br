---
description: Opções de SSPI para aplicativos distribuídos
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opções de SSPI para aplicativos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826771"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="4fa69-103">Opções de SSPI para aplicativos distribuídos</span><span class="sxs-lookup"><span data-stu-id="4fa69-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="4fa69-104">Os desenvolvedores têm muitas opções para a criação de aplicativos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="4fa69-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="4fa69-105">A [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) fornece uma camada de abstração entre protocolos de nível de aplicativo e protocolos de [*segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4fa69-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="4fa69-106">Os aplicativos podem aproveitar os protocolos de segurança SSPI de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="4fa69-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="4fa69-107">Chame as rotinas SSPI diretamente (para aplicativos tradicionais baseados em soquete).</span><span class="sxs-lookup"><span data-stu-id="4fa69-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="4fa69-108">As rotinas usam mensagens de solicitação/resposta para implementar o [*protocolo de aplicativo*](../secgloss/a-gly.md) que transporta dados do SSPI relacionados à segurança.</span><span class="sxs-lookup"><span data-stu-id="4fa69-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="4fa69-109">Use COM para chamar opções de segurança que são implementadas usando RPC autenticado e SSPI em níveis inferiores.</span><span class="sxs-lookup"><span data-stu-id="4fa69-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="4fa69-110">Esses aplicativos não chamam funções SSPI diretamente.</span><span class="sxs-lookup"><span data-stu-id="4fa69-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="4fa69-111">Use o [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) com a interface do Winsock estendida para permitir que os provedores de transporte usem recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="4fa69-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="4fa69-112">Essa abordagem integra o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) à pilha de rede e fornece serviços de segurança e transporte por meio de uma interface comum.</span><span class="sxs-lookup"><span data-stu-id="4fa69-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="4fa69-113">Use a [API do Windows Internet Extensions](../wininet/portal.md) (Wininet) e uma interface projetada para oferecer suporte a protocolos de segurança da Internet, como o protocolo [*protocolo SSL*](../secgloss/s-gly.md) (SSL).</span><span class="sxs-lookup"><span data-stu-id="4fa69-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="4fa69-114">Os aplicativos usam a interface SSPI para o provedor de segurança do [canal seguro](secure-channel.md) (Schannel) para implementar a segurança do Wininet.</span><span class="sxs-lookup"><span data-stu-id="4fa69-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="4fa69-115">O Schannel é a implementação do SSL da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4fa69-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="4fa69-116">Várias funções SSPI retornam carimbos de data/hora que representam o período de vida de vários objetos.</span><span class="sxs-lookup"><span data-stu-id="4fa69-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="4fa69-117">Os [*pacotes de segurança*](../secgloss/s-gly.md) podem manter o tempo e fornecer carimbos de data/hora de maneiras diferentes, mas usar a hora local simplifica o trabalho dos aplicativos que usam funções SSPI.</span><span class="sxs-lookup"><span data-stu-id="4fa69-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
