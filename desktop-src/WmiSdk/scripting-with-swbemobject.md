---
description: O objeto de script SWbemObject é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto SWbemObject está associado.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Criando scripts com SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091300"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="e7226-103">Criando scripts com SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e7226-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="e7226-104">O objeto de script [**SWbemObject**](swbemobject.md) é o objeto WMI genérico, definindo propriedades e métodos que podem ser usados independentemente do objeto WMI específico ao qual o objeto **SWbemObject** está associado.</span><span class="sxs-lookup"><span data-stu-id="e7226-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="e7226-105">Todos os objetos WMI, como uma instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou qualquer outra classe de dados WMI, são representados por [**SWbemObject**](swbemobject.md) e podem usar os métodos e propriedades comuns de **SWbemObject** , além de suas próprias propriedades e métodos específicos.</span><span class="sxs-lookup"><span data-stu-id="e7226-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="e7226-106">Por exemplo, use o script a seguir para obter todas as instâncias de um [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) chamando o método [**SWbemObject. Instances \_**](swbemobject-instances-.md) .</span><span class="sxs-lookup"><span data-stu-id="e7226-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="e7226-107">O clsobjProcess representa a definição de classe de **\_ processo do Win32** e um [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="e7226-108">O exemplo a seguir obtém uma instância específica do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa o serviço de alerta e o armazena em objAlerter.</span><span class="sxs-lookup"><span data-stu-id="e7226-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="e7226-109">Em seguida, você pode chamar os métodos [**SWbemObject**](swbemobject.md) , como WScript. Echo ObjAlerter. Path \_ , ou métodos definidos pela classe de dados, como WScript. Echo objAlerter. State.</span><span class="sxs-lookup"><span data-stu-id="e7226-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="e7226-110">objAlerter que representa uma instância do serviço Win32 \_ e um **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="e7226-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="e7226-111">A chamada para [**SWbemObject. Instances \_**](swbemobject-instances-.md) Obtém outro objeto de script WMI genérico, [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="e7226-112">Como mostrado, o objeto **SWbemObjectSet** pode ser tratado como uma [coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="e7226-113">Você pode identificar os métodos [**SWbemObject**](swbemobject.md) porque todos eles terminam com um sublinhado ( \_ ), por exemplo, [**SWbemObject \_ . Instances**](swbemobject-instances-.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="e7226-114">[**SWbemObjectEx**](swbemobjectex.md) estende as propriedades de [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="e7226-115">Por exemplo, agora você pode atualizar os dados de qualquer objeto WMI, como uma instância do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process), por uma chamada para [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="e7226-116">O exemplo a seguir mostra como os dados de falha de página do processo do sistema podem ser atualizados a cada cinco segundos.</span><span class="sxs-lookup"><span data-stu-id="e7226-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="e7226-117">Para obter mais informações sobre como atualizar dados usando um objeto [**SWbemRefresher**](swbemrefresher.md) , consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="e7226-118">O [**SWbemObject. put \_**](swbemobject-put-.md) e [**o \_ PutAsync**](swbemobject-putasync-.md) permitem que você grave alterações de volta em qualquer objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="e7226-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="e7226-119">Esses métodos só confirmam alterações em um objeto no namespace em que o objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="e7226-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="e7226-120">Você pode gravar o objeto em um namespace diferente usando [**SWbemServicesEx. put**](swbemservicesex-put.md) ou [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).</span><span class="sxs-lookup"><span data-stu-id="e7226-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7226-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7226-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7226-122">API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="e7226-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="e7226-123">Criando um script WMI</span><span class="sxs-lookup"><span data-stu-id="e7226-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="e7226-124">Atualizando uma instância inteira</span><span class="sxs-lookup"><span data-stu-id="e7226-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="e7226-125">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="e7226-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
