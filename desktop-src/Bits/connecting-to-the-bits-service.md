---
title: Conectando-se ao serviço BITS
description: Para se conectar ao serviço BITS, crie uma instância do objeto BackgroundCopyManager, conforme mostrado no exemplo a seguir.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084654"
---
# <a name="connecting-to-the-bits-service"></a>Conectando-se ao serviço BITS

Para se conectar ao serviço do sistema BITS, crie uma instância do objeto BackgroundCopyManager, conforme mostrado no exemplo a seguir. O serviço do sistema BITS é o serviço de sistema do Windows em execução no computador cliente que implementa o recurso de transferência em segundo plano.


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



Para testar uma versão específica do BITS, use um identificador de classe simbólico para o BackgroundCopyManager com base na versão que você deseja verificar. Por exemplo, para testar o BITS 10,2, use CLSID \_ BackgroundCopyManager10 \_ 2.

O exemplo a seguir mostra como usar um dos identificadores de classe simbólicos.


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



Use os métodos da interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para [criar trabalhos de transferência](creating-a-job.md), [enumerar trabalhos](enumerating-jobs-in-the-transfer-queue.md) na fila e [recuperar trabalhos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



O BITS requer que os proxies de interface do cliente usem o nível identificar ou representar a representação. Se o aplicativo não chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), o com usará identificar por padrão. BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido. Se você fornecer uma biblioteca que exercita as interfaces BITS e um aplicativo que chama sua biblioteca definir o nível de representação abaixo de identificar, será necessário chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir o nível de representação correto para cada interface de bits que você chamar.

Antes de o aplicativo sair, libere a cópia do ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , conforme mostrado no exemplo a seguir.


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

[Chamando em bits do .net e do C#](/windows/desktop/Bits/bits-dot-net) para bits
</dt> </dl>

 

 