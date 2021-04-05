---
description: Depois de definir os níveis de segurança para o ponteiro de IWbemServices, você pode acessar os vários recursos do WMI. Depois de terminar de usar o WMI, você deve desligar o aplicativo.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Limpando e desligando um aplicativo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922204"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="5f92c-104">Limpando e desligando um aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="5f92c-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="5f92c-105">Depois de definir os níveis de segurança para o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , você pode acessar os vários recursos do WMI.</span><span class="sxs-lookup"><span data-stu-id="5f92c-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="5f92c-106">Depois de terminar de usar o WMI, você deve desligar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f92c-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="5f92c-107">O procedimento a seguir descreve como limpar e desligar um aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="5f92c-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="5f92c-108">**Para limpar e desligar um aplicativo WMI**</span><span class="sxs-lookup"><span data-stu-id="5f92c-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="5f92c-109">Libere qualquer interface COM aberta.</span><span class="sxs-lookup"><span data-stu-id="5f92c-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="5f92c-110">As duas interfaces primárias que você deve lembrar para liberação são [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="5f92c-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="5f92c-111">Chame [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="5f92c-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="5f92c-112">Assim como em todos os aplicativos COM, você deve chamar [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) no final do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f92c-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="5f92c-113">Saia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f92c-113">Exit your application.</span></span>

    <span data-ttu-id="5f92c-114">O exemplo de código a seguir mostra como sair de um aplicativo cliente WMI.</span><span class="sxs-lookup"><span data-stu-id="5f92c-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="5f92c-115">A `pSvc` variável é do tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* e a variável PLoc é do tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="5f92c-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="5f92c-116">Agora você inicializou com êxito o COM, o WMI acessado e saiu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f92c-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="5f92c-117">Para obter mais informações, consulte [exemplo: Criando um aplicativo WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="5f92c-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f92c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f92c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f92c-119">Criando um aplicativo WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="5f92c-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
