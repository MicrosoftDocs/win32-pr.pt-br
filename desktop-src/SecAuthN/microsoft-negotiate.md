---
description: O Microsoft Negotiate é um provedor de suporte de segurança que atua como uma camada de aplicativo entre a interface do provedor de suporte de segurança e os outros SSPs.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920854"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="9c1d0-103">Microsoft Negotiate</span><span class="sxs-lookup"><span data-stu-id="9c1d0-103">Microsoft Negotiate</span></span>

<span data-ttu-id="9c1d0-104">O Microsoft Negotiate é um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) que atua como uma camada de aplicativo entre o [SSPI](sspi.md)( [*Security Support Provider interface*](../secgloss/s-gly.md) ) e outros SSPs.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="9c1d0-105">Quando um aplicativo chama o SSPI para fazer logon em uma rede, ele pode especificar um SSP para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="9c1d0-106">Se o aplicativo especificar Negotiate, Negotiate analisará a solicitação e escolherá o melhor SSP para lidar com a solicitação com base na política de segurança configurada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="9c1d0-107">Atualmente, o pacote de segurança Negotiate seleciona entre [Kerberos](microsoft-kerberos.md) e [NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="9c1d0-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="9c1d0-108">Negociar seleciona Kerberos, a menos que não possa ser usado por um dos sistemas envolvidos na autenticação ou o aplicativo de chamada não forneceu informações suficientes para usar o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="9c1d0-109">Para permitir que o Negotiate selecione o provedor de segurança [Kerberos](microsoft-kerberos.md) , o aplicativo cliente deve fornecer um [*nome da entidade de serviço*](../secgloss/s-gly.md) (SPN), um nome UPN ou um nome de conta NetBIOS como o nome de destino.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="9c1d0-110">Caso contrário, Negotiate sempre seleciona o provedor de segurança [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1d0-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="9c1d0-111">Um servidor que usa o pacote Negotiate é capaz de responder a aplicativos cliente que selecionam especificamente o provedor de segurança [Kerberos](microsoft-kerberos.md) ou [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1d0-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="9c1d0-112">No entanto, um aplicativo cliente deve saber que um servidor dá suporte ao pacote Negotiate para solicitar autenticação usando Negotiate.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="9c1d0-113">Um servidor que não dá suporte a Negotiate nem sempre responde a solicitações de clientes que especificam Negotiate como o SSP.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="9c1d0-114">Motivos para usar o pacote Negotiate</span><span class="sxs-lookup"><span data-stu-id="9c1d0-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="9c1d0-115">Permite que o sistema use o protocolo mais forte (mais seguro) disponível.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="9c1d0-116">Garante a compatibilidade de encaminhamento para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="9c1d0-117">Garante que seu aplicativo exiba o comportamento que está de acordo com a política de segurança definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="9c1d0-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
