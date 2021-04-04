---
title: Testando se em execução em um controlador de domínio
description: O código a seguir usa a função VerifyVersionInfo para determinar se o processo de chamada está em execução em um controlador de domínio do Windows 2000 Server.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084429"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="bbc7a-103">Testando se em execução em um controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="bbc7a-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="bbc7a-104">O código a seguir usa a função [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) para determinar se o processo de chamada está em execução em um controlador de domínio do Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="bbc7a-105">O programa de instalação do serviço pode usar esse teste antes de instalar um serviço na conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="bbc7a-106">Se o teste indicar que você está sendo executado em um controlador de domínio, você instalará o serviço para ser executado em uma conta de usuário ou exibirá um aviso de caixa de diálogo dos perigos em execução como LocalSystem em um controlador de domínio (que, em seguida, o serviço teria acesso irrestrito ao Active Directory Domain Services, um contexto de segurança poderoso extremamente que tem o potencial de danificar toda a rede).</span><span class="sxs-lookup"><span data-stu-id="bbc7a-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 