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
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>Compondo os SPNs de um serviço com um SCP

O exemplo de código a seguir compõe um SPN para um serviço que usa um SCP (ponto de conexão de serviço). O SPN retornado tem o seguinte formato.


```C++
<service class>/<host>/<service name>
```



" &lt; classe &gt; de serviço" e " &lt; nome &gt; do serviço" correspondem aos parâmetros *pszDNofSCP* e *pszServiceClass* . o &lt; padrão "host &gt; " é o nome DNS do computador local.


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



 

 




