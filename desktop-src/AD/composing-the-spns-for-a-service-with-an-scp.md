---
title: Compondo os SPNs de um serviço com um SCP
description: O exemplo de código a seguir compõe um SPN para um serviço que usa um SCP (ponto de conexão de serviço).
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Compor os SPNs de um serviço com um SCP AD
- Nome da entidade de serviço anúncio, compondo SPNs para um serviço com um SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004813"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a><span data-ttu-id="f5cd9-105">Compondo os SPNs de um serviço com um SCP</span><span class="sxs-lookup"><span data-stu-id="f5cd9-105">Composing the SPNs for a Service with an SCP</span></span>

<span data-ttu-id="f5cd9-106">O exemplo de código a seguir compõe um SPN para um serviço que usa um SCP (ponto de conexão de serviço).</span><span class="sxs-lookup"><span data-stu-id="f5cd9-106">The following code example composes an SPN for a service that uses a service connection point (SCP).</span></span> <span data-ttu-id="f5cd9-107">O SPN retornado tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="f5cd9-107">The returned SPN has the following format.</span></span>


```C++
<service class>/<host>/<service name>
```



<span data-ttu-id="f5cd9-108">" &lt; classe &gt; de serviço" e " &lt; nome &gt; do serviço" correspondem aos parâmetros *pszDNofSCP* e *pszServiceClass* .</span><span class="sxs-lookup"><span data-stu-id="f5cd9-108">"&lt;service class&gt;" and "&lt;service name&gt;" correspond to the *pszDNofSCP* and *pszServiceClass* parameters.</span></span> <span data-ttu-id="f5cd9-109">o &lt; padrão "host &gt; " é o nome DNS do computador local.</span><span class="sxs-lookup"><span data-stu-id="f5cd9-109">"&lt;host&gt;" defaults to the DNS name of the local computer.</span></span>


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




