---
title: Conectando-se ao serviço BITS
description: Para se conectar ao serviço BITS, crie uma instância do objeto BackgroundCopyManager, conforme mostrado no exemplo a seguir.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528936"
---
# <a name="connecting-to-the-bits-service"></a>Conectando-se ao serviço BITS

Para se conectar ao serviço de sistema BITS, crie uma instância do objeto BackgroundCopyManager, conforme mostrado no exemplo a seguir. O serviço de sistema BITS é o Windows do sistema em execução no computador cliente que implementa a funcionalidade de transferência em segundo plano.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



Para testar uma versão específica do BITS, use um identificador de classe simbólico para BackgroundCopyManager com base na versão que você deseja verificar. Por exemplo, para testar o BITS 10.2, use o \_ BackgroundCopyManager10 2 do \_ CLSID.

O exemplo a seguir mostra como usar um dos identificadores de classe simbólico.


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



Use os métodos da interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para criar trabalhos de [transferência,](creating-a-job.md) [enumerar](enumerating-jobs-in-the-transfer-queue.md) trabalhos na fila e [recuperar trabalhos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



O BITS requer que os proxies de interface do cliente usem o nível de representação IDENTIFY ou IMPERSONATE. Se o aplicativo não chamar [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)COM usará IDENTIFY por padrão. BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido. Se você fornecer uma biblioteca que exerce as interfaces BITS e um aplicativo que chama sua biblioteca definir o nível de representação abaixo de IDENTIFY, você precisará chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir o nível de representação correto para cada interface BITS que você chamar.

Antes de seu aplicativo ser final, libere sua cópia do ponteiro de interface [**IBackgroundCopyManager,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) conforme mostrado no exemplo a seguir.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando em BITS do .NET e C#](/windows/desktop/Bits/bits-dot-net) para BITS
</dt> </dl>

 

 