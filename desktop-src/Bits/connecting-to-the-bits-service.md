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
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="00d92-103">Conectando-se ao serviço BITS</span><span class="sxs-lookup"><span data-stu-id="00d92-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="00d92-104">Para se conectar ao serviço do sistema BITS, crie uma instância do objeto BackgroundCopyManager, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="00d92-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="00d92-105">O serviço do sistema BITS é o serviço de sistema do Windows em execução no computador cliente que implementa o recurso de transferência em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="00d92-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


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



<span data-ttu-id="00d92-106">Para testar uma versão específica do BITS, use um identificador de classe simbólico para o BackgroundCopyManager com base na versão que você deseja verificar.</span><span class="sxs-lookup"><span data-stu-id="00d92-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="00d92-107">Por exemplo, para testar o BITS 10,2, use CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="00d92-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="00d92-108">O exemplo a seguir mostra como usar um dos identificadores de classe simbólicos.</span><span class="sxs-lookup"><span data-stu-id="00d92-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


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



<span data-ttu-id="00d92-109">Use os métodos da interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) para [criar trabalhos de transferência](creating-a-job.md), [enumerar trabalhos](enumerating-jobs-in-the-transfer-queue.md) na fila e [recuperar trabalhos](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="00d92-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="00d92-110">O BITS requer que os proxies de interface do cliente usem o nível identificar ou representar a representação.</span><span class="sxs-lookup"><span data-stu-id="00d92-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="00d92-111">Se o aplicativo não chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), o com usará identificar por padrão.</span><span class="sxs-lookup"><span data-stu-id="00d92-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="00d92-112">BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="00d92-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="00d92-113">Se você fornecer uma biblioteca que exercita as interfaces BITS e um aplicativo que chama sua biblioteca definir o nível de representação abaixo de identificar, será necessário chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir o nível de representação correto para cada interface de bits que você chamar.</span><span class="sxs-lookup"><span data-stu-id="00d92-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="00d92-114">Antes de o aplicativo sair, libere a cópia do ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="00d92-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="00d92-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00d92-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="00d92-116">[Chamando em bits do .net e do C#](/windows/desktop/Bits/bits-dot-net) para bits</span><span class="sxs-lookup"><span data-stu-id="00d92-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 