---
title: Testando se está em execução em um controlador de domínio
description: O código a seguir usa a função VerifyVersionInfo para determinar se o processo de chamada está em execução em um controlador de domínio Windows 2000 Server.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024584"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Testando se está em execução em um controlador de domínio

O código a seguir usa a [**função VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) para determinar se o processo de chamada está em execução em um controlador de domínio Windows 2000 Server. Seu programa de instalação de serviço pode usar esse teste antes de instalar um serviço na conta LocalSystem. Se o teste indicar que você está executando em um controlador de domínio, instale o serviço para ser executado em uma conta de usuário ou exadibile uma caixa de diálogo de aviso dos riscos na execução como LocalSystem em um controlador de domínio (que é o fato de que o serviço teria acesso irrestrito ao Active Directory Domain Services, um contexto de segurança extremamente poderoso que tem o potencial de danificar toda a rede).


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



 

 