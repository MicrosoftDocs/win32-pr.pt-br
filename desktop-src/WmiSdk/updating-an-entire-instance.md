---
description: O meio mais comum de atualizar uma instância de classe WMI é atualizar toda a instância de uma vez.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Atualizando uma instância inteira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170603"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="db4b4-103">Atualizando uma instância inteira</span><span class="sxs-lookup"><span data-stu-id="db4b4-103">Updating an Entire Instance</span></span>

<span data-ttu-id="db4b4-104">O meio mais comum de atualizar uma instância de classe WMI é atualizar toda a instância de uma vez.</span><span class="sxs-lookup"><span data-stu-id="db4b4-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="db4b4-105">Ao atualizar uma instância inteira, o WMI não precisa analisar a instância em propriedades individuais e enviá-las ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db4b4-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="db4b4-106">Em vez disso, o WMI pode simplesmente enviar a você a instância inteira.</span><span class="sxs-lookup"><span data-stu-id="db4b4-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="db4b4-107">Quando você terminar, o WMI poderá copiar toda a instância alterada na instância original.</span><span class="sxs-lookup"><span data-stu-id="db4b4-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="db4b4-108">O procedimento a seguir descreve como modificar ou atualizar uma instância usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db4b4-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="db4b4-109">**Para modificar ou atualizar uma instância usando o PowerShell**</span><span class="sxs-lookup"><span data-stu-id="db4b4-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="db4b4-110">Recupere uma cópia local do objeto com uma chamada para Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="db4b4-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="db4b4-111">Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.</span><span class="sxs-lookup"><span data-stu-id="db4b4-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="db4b4-112">Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.</span><span class="sxs-lookup"><span data-stu-id="db4b4-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="db4b4-113">Faça as alterações nas propriedades do objeto local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="db4b4-114">Isso altera apenas a cópia local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="db4b4-115">Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="db4b4-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="db4b4-116">Coloque o objeto de volta no repositório WMI usando uma chamada para o método Put.</span><span class="sxs-lookup"><span data-stu-id="db4b4-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="db4b4-117">O procedimento a seguir descreve como modificar ou atualizar uma instância usando C#.</span><span class="sxs-lookup"><span data-stu-id="db4b4-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="db4b4-118">**Para modificar ou atualizar uma instância usando C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="db4b4-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="db4b4-119">Recupere uma cópia local do objeto com uma chamada para [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), conforme descrito em [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="db4b4-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="db4b4-120">Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.</span><span class="sxs-lookup"><span data-stu-id="db4b4-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="db4b4-121">Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.</span><span class="sxs-lookup"><span data-stu-id="db4b4-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="db4b4-122">Faça as alterações nas propriedades do objeto local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="db4b4-123">Isso altera apenas a cópia local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="db4b4-124">Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="db4b4-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="db4b4-125">Coloque o objeto de volta no repositório WMI usando uma chamada para [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db4b4-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="db4b4-126">O procedimento a seguir descreve como modificar ou atualizar uma instância usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db4b4-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="db4b4-127">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="db4b4-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="db4b4-128">**Para modificar ou atualizar uma instância usando C# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="db4b4-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="db4b4-129">Recupere uma cópia local do objeto com uma chamada para [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="db4b4-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="db4b4-130">Se necessário, exiba as propriedades do objeto com uma chamada para a coleção de propriedades.</span><span class="sxs-lookup"><span data-stu-id="db4b4-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="db4b4-131">Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.</span><span class="sxs-lookup"><span data-stu-id="db4b4-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="db4b4-132">Faça as alterações nas propriedades do objeto local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="db4b4-133">Isso altera apenas a cópia local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="db4b4-134">Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="db4b4-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="db4b4-135">Coloque o objeto de volta no repositório WMI usando uma chamada para o método [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) ou.</span><span class="sxs-lookup"><span data-stu-id="db4b4-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="db4b4-136">O procedimento a seguir descreve como modificar ou atualizar uma instância usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="db4b4-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="db4b4-137">**Para modificar ou atualizar uma instância usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="db4b4-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="db4b4-138">Recupere uma cópia local do objeto com uma chamada para **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="db4b4-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="db4b4-139">Se necessário, exiba as propriedades do objeto com uma chamada para o método [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="db4b4-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="db4b4-140">Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.</span><span class="sxs-lookup"><span data-stu-id="db4b4-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="db4b4-141">Faça as alterações nas propriedades do objeto com uma chamada para o método [**SWbemProperty. Value**](swbemproperty-value.md) .</span><span class="sxs-lookup"><span data-stu-id="db4b4-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="db4b4-142">O método **Value** altera apenas a cópia local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="db4b4-143">Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="db4b4-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="db4b4-144">Coloque o objeto de volta no repositório WMI com uma chamada para os métodos [**SWbemObject \_ . put**](swbemobject-put-.md) ou [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="db4b4-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="db4b4-145">Como os nomes sugerem, [**Coloque \_**](swbemobject-put-.md) atualizações de forma síncrona enquanto o [**PutAsync \_**](swbemobject-putasync-.md) atualiza de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="db4b4-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="db4b4-146">O método copia sobre a instância original com sua instância modificada.</span><span class="sxs-lookup"><span data-stu-id="db4b4-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="db4b4-147">No entanto, para aproveitar o processamento assíncrono, você deve criar um objeto [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="db4b4-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="db4b4-148">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="db4b4-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="db4b4-149">O procedimento a seguir descreve como modificar ou atualizar uma instância usando C++.</span><span class="sxs-lookup"><span data-stu-id="db4b4-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="db4b4-150">**Para modificar ou atualizar uma instância usando C++**</span><span class="sxs-lookup"><span data-stu-id="db4b4-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="db4b4-151">Recupere uma cópia local da instância com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="db4b4-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="db4b4-152">Se necessário, exiba as propriedades do objeto com uma chamada para [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span><span class="sxs-lookup"><span data-stu-id="db4b4-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="db4b4-153">Embora não seja necessário, talvez você queira saber o valor da propriedade antes de alterá-la.</span><span class="sxs-lookup"><span data-stu-id="db4b4-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="db4b4-154">Faça as alterações necessárias na cópia com uma chamada para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="db4b4-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="db4b4-155">O método **Put** altera apenas a cópia local.</span><span class="sxs-lookup"><span data-stu-id="db4b4-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="db4b4-156">Para salvar as alterações no WMI, você deve posicionar toda a cópia de volta no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="db4b4-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="db4b4-157">Coloque sua cópia de volta no repositório WMI com uma chamada de [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) métodos de utinstanceasync.</span><span class="sxs-lookup"><span data-stu-id="db4b4-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="db4b4-158">Como os nomes sugerem, a **PutInstance** é atualizada de forma síncrona enquanto [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) atualiza de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="db4b4-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="db4b4-159">O método copia sobre a instância original com sua instância modificada.</span><span class="sxs-lookup"><span data-stu-id="db4b4-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="db4b4-160">No entanto, para aproveitar o processamento assíncrono, você deve implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="db4b4-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="db4b4-161">Você deve estar ciente de que uma operação de atualização em uma instância que pertence a uma hierarquia de classe pode não ter sucesso devido a um erro envolvendo outra classe na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="db4b4-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="db4b4-162">O WMI chama o método [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de cada um dos provedores responsáveis pelas classes das quais a classe proprietária da instância original deriva.</span><span class="sxs-lookup"><span data-stu-id="db4b4-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="db4b4-163">Se qualquer um desses provedores falhar, a solicitação de atualização original falhará.</span><span class="sxs-lookup"><span data-stu-id="db4b4-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="db4b4-164">Para obter mais informações, consulte a seção comentários de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="db4b4-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="db4b4-165">Para obter mais informações, consulte [chamando um método de provedor](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="db4b4-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="db4b4-166">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="db4b4-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="db4b4-167">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="db4b4-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
