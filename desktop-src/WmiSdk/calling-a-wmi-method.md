---
title: Como chamar um método WMI
description: A principal finalidade do WMI é fornecer acesso a classes e instâncias que representam objetos em sua rede.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506028"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="2f08f-103">Como chamar um método WMI</span><span class="sxs-lookup"><span data-stu-id="2f08f-103">How to call a WMI method</span></span>

<span data-ttu-id="2f08f-104">A principal finalidade do WMI é fornecer acesso a classes e instâncias que representam objetos em sua rede.</span><span class="sxs-lookup"><span data-stu-id="2f08f-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="2f08f-105">Essas classes e instâncias têm suporte dos provedores do.</span><span class="sxs-lookup"><span data-stu-id="2f08f-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="2f08f-106">Por exemplo, todas as instâncias que representam dispositivos de hardware padrão em sua empresa, como [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) ou a [**\_ impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), são suportadas pelo provedor Win32.</span><span class="sxs-lookup"><span data-stu-id="2f08f-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="2f08f-107">Da mesma forma, você pode acessar o log de eventos por meio do provedor de log de eventos e o registro por meio do provedor de registro.</span><span class="sxs-lookup"><span data-stu-id="2f08f-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="2f08f-108">Os métodos que o WMI implementa em interfaces como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou scripting Objects, como [**SWbemServices**](swbemservices.md), são basicamente para obter e manipular genericamente os dados fornecidos por qualquer provedor.</span><span class="sxs-lookup"><span data-stu-id="2f08f-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="2f08f-109">Por exemplo, use [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) para obter todas as instâncias do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) em um subconjunto de computadores empresariais.</span><span class="sxs-lookup"><span data-stu-id="2f08f-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="2f08f-110">Em seguida, você pode chamar o método do provedor Win32 [**Getownerid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) em cada objeto de **\_ processo do Win32** .</span><span class="sxs-lookup"><span data-stu-id="2f08f-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="2f08f-111">No exemplo a seguir, o método [**Getownerid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) é chamado como um método de automação no objeto de processo.</span><span class="sxs-lookup"><span data-stu-id="2f08f-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="2f08f-112">Um método WMI, como o método [**de \_ caminho**](swbemobject-path-.md) definido para [**SWbemObject**](swbemobject.md) também pode ser chamado no objeto de **processo** .</span><span class="sxs-lookup"><span data-stu-id="2f08f-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="2f08f-113">O processo real de usar os métodos WMI é idêntico ao uso de qualquer outra interface COM ou de automação do Windows.</span><span class="sxs-lookup"><span data-stu-id="2f08f-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="2f08f-114">Para obter mais informações, consulte [com](../cossdk/component-services-portal.md) e [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="2f08f-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="2f08f-115">Para obter mais informações sobre as interfaces às quais o WMI dá suporte, consulte [API com para WMI](com-api-for-wmi.md) e [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2f08f-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="2f08f-116">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="2f08f-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f08f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f08f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f08f-118">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="2f08f-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
