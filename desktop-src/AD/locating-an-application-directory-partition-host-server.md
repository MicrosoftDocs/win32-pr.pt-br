---
title: Localizando um servidor de host de partição de diretório de aplicativo
description: Este tópico descreve como localizar um servidor de host de partição de diretório de aplicativo.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Localizando um servidor host de partição de diretório de aplicativo AD
- AD de partições de diretório de aplicativo, localizando um servidor host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634937"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="182c0-105">Localizando um servidor de host de partição de diretório de aplicativo</span><span class="sxs-lookup"><span data-stu-id="182c0-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="182c0-106">O serviço NetLogon registra a seguinte lista de registros SRV para uma partição de diretório de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="182c0-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="182c0-107">\_LDAP. \_ Protocol.<partition name></span><span class="sxs-lookup"><span data-stu-id="182c0-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="182c0-108">\_LDAP. \_ TCP. <site name> . \_ sites.<partition name></span><span class="sxs-lookup"><span data-stu-id="182c0-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="182c0-109">Para localizar um controlador de domínio que hospede uma réplica de uma partição de diretório de aplicativo especificada, chame a função [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) com o parâmetro *DomainName* definido como o nome DNS da partição de diretório de aplicativo e o sinalizador **\_ somente \_ LDAP \_ necessário** definido no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="182c0-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="182c0-110">Para obter mais informações e um exemplo de código que mostra, usando a função **DsGetDcName** , como localizar um controlador de domínio que hospeda uma réplica de uma partição de diretório de aplicativos, consulte [código de exemplo para localizar um servidor de host de partição de diretório de aplicativo](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="182c0-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




