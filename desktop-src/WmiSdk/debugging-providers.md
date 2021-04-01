---
description: Os provedores, a menos que sejam dissociados provedores em execução em um aplicativo, sejam carregados em um processo de Wmiprvse.exe e não por meio de Svchost.exe com um processo de Winmgmt.exe. Para obter mais informações, consulte provedor de hospedagem e segurança.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Provedores de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921359"
---
# <a name="debugging-providers"></a><span data-ttu-id="f628b-104">Provedores de depuração</span><span class="sxs-lookup"><span data-stu-id="f628b-104">Debugging Providers</span></span>

<span data-ttu-id="f628b-105">Os provedores, a menos que sejam [*dissociados provedores*](gloss-d.md) em execução em um aplicativo, sejam carregados em um processo de Wmiprvse.exe e não por meio de Svchost.exe com um processo de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="f628b-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="f628b-106">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f628b-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="f628b-107">Ao parar em um ponto de interrupção, o depurador do Visual Studio congela todo o processo de host do provedor, que geralmente é o host compartilhado Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="f628b-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="f628b-108">Isso impede a operação de quaisquer outros componentes hospedados nesse processo, incluindo a extensão de Gerenciador de Servidores WMI.</span><span class="sxs-lookup"><span data-stu-id="f628b-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="f628b-109">Os aplicativos cliente que chamam o provedor também são bloqueados.</span><span class="sxs-lookup"><span data-stu-id="f628b-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="f628b-110">Os problemas resultantes são piores no Windows 2000 e anteriores, pois o provedor é carregado no processo de serviço WMI (Winmgmt.exe).</span><span class="sxs-lookup"><span data-stu-id="f628b-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="f628b-111">Se você executar o WMI Gerenciador de Servidores em outra instância, o IDE do Visual Studio não congelará e você poderá liberar o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="f628b-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="f628b-112">É recomendável que você execute seu provedor em um processo de hospedagem separado durante a fase de desenvolvimento, para que a interrupção em um ponto de interrupção apenas congele o processo que hospeda seu provedor.</span><span class="sxs-lookup"><span data-stu-id="f628b-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="f628b-113">As outras funções no WMI continuam acessíveis para o WMI Gerenciador de Servidores e quaisquer outros aplicativos ou scripts baseados em WMI.</span><span class="sxs-lookup"><span data-stu-id="f628b-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="f628b-114">Além disso, se o seu provedor falhar, ele não afetará a operação de outros provedores carregados no mesmo processo de host.</span><span class="sxs-lookup"><span data-stu-id="f628b-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="f628b-115">Para fazer com que seu provedor seja carregado em seu próprio processo de host, modifique o registro do provedor para definir a propriedade [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) para `NetworkServiceHost:[MyProvider]` onde MyProvider pode ser qualquer cadeia de caracteres que identifique exclusivamente seu provedor.</span><span class="sxs-lookup"><span data-stu-id="f628b-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="f628b-116">Por exemplo, use o valor **\_ \_ Win32Provider. CLSID** .</span><span class="sxs-lookup"><span data-stu-id="f628b-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="f628b-117">Quando seu provedor estiver pronto para ser entregue, retorne o **\_ \_ Win32Provider. HostingModel** para o valor pretendido, como **NetworkServiceHost**.</span><span class="sxs-lookup"><span data-stu-id="f628b-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="f628b-118">Se você não estiver depurando o carregamento do provedor, você pode chamar o [**método Load da \_ classe de provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) para forçar o carregamento do seu provedor e, em seguida, anexar ao processo de Wmiprvse.exe que tem a DLL carregada e depurar conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f628b-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f628b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f628b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f628b-120">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="f628b-120">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="f628b-121">Classes de solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="f628b-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
