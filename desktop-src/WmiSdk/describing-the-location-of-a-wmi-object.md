---
description: Conceitualmente semelhante a um Uniform Resource Locator (URL), um caminho de objeto WMI é uma cadeia de caracteres que identifica exclusivamente o namespace em um servidor, uma classe dentro de um namespace ou instâncias de uma classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Descrevendo o local de um objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787783"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="a7de1-103">Descrevendo o local de um objeto WMI</span><span class="sxs-lookup"><span data-stu-id="a7de1-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="a7de1-104">Conceitualmente semelhante a um Uniform Resource Locator (URL), um caminho de objeto WMI é uma cadeia de caracteres que identifica exclusivamente o namespace em um servidor, uma classe dentro de um namespace ou instâncias de uma classe.</span><span class="sxs-lookup"><span data-stu-id="a7de1-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="a7de1-105">Um caminho de objeto é hierárquico e contém vários elementos que descrevem o local do objeto em questão.</span><span class="sxs-lookup"><span data-stu-id="a7de1-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="a7de1-106">Assim como os caminhos de arquivo, os caminhos de objeto do WMI podem ser descritos em completo ou especificado como um caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="a7de1-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="a7de1-107">O namespace de um objeto WMI é listado na página de referência do WMI.</span><span class="sxs-lookup"><span data-stu-id="a7de1-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="a7de1-108">Por exemplo, o local da maioria das classes com suporte nos [provedores WMI CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) está localizado no \\ \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="a7de1-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="a7de1-109">O código do PowerShell a seguir descreve uma chamada para recuperar o objeto de [**\_ ComputerSystem do Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) em seu computador local:</span><span class="sxs-lookup"><span data-stu-id="a7de1-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="a7de1-110">Como alternativa, uma instância específica do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pode ter o seguinte caminho da propriedade [**SWbemObject. \_ Path**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="a7de1-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="a7de1-111">O exemplo a seguir mostra o caminho relativo para essa instância, como visto exibindo a propriedade [**RelPath**](swbemobjectpath-relpath.md) do objeto [**SWbemObjectPath**](swbemobjectpath.md) retornado pela chamada para [**SWbemObject. Path \_**](swbemobject-path-.md).</span><span class="sxs-lookup"><span data-stu-id="a7de1-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="a7de1-112">Observe que **DeviceID** é a propriedade de chave da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="a7de1-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="a7de1-113">C++</span><span class="sxs-lookup"><span data-stu-id="a7de1-113">C++</span></span>

<span data-ttu-id="a7de1-114">A tabela a seguir lista os tipos de caminho de objeto e os métodos associados que exigem caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="a7de1-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7de1-115">Tipo de caminho do objeto</span><span class="sxs-lookup"><span data-stu-id="a7de1-115">Object path type</span></span></th>
<th><span data-ttu-id="a7de1-116">Método</span><span class="sxs-lookup"><span data-stu-id="a7de1-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7de1-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span><span class="sxs-lookup"><span data-stu-id="a7de1-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="a7de1-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7de1-119"><a href="describing-a-class-object-path.md">Classe</a></span><span class="sxs-lookup"><span data-stu-id="a7de1-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="a7de1-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="a7de1-121">[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span><span class="sxs-lookup"><span data-stu-id="a7de1-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7de1-122"><a href="describing-a-class-object-path.md">Classe</a> ou <a href="describing-an-instance-object-path.md">instância</a></span><span class="sxs-lookup"><span data-stu-id="a7de1-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="a7de1-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="a7de1-124">[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span><span class="sxs-lookup"><span data-stu-id="a7de1-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7de1-125"><a href="describing-an-instance-object-path.md">Instância</a></span><span class="sxs-lookup"><span data-stu-id="a7de1-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="a7de1-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="a7de1-127">[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span><span class="sxs-lookup"><span data-stu-id="a7de1-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="a7de1-128">Script</span><span class="sxs-lookup"><span data-stu-id="a7de1-128">Script</span></span>

<span data-ttu-id="a7de1-129">Os caminhos de objeto podem ser construídos de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="a7de1-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="a7de1-130">Recupere a propriedade de um método que retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="a7de1-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="a7de1-131">Recupere a propriedade [**SWbemObject. \_ Path**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="a7de1-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="a7de1-132">Crie uma variável de cadeia de caracteres que contenha o caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="a7de1-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="a7de1-133">A tabela a seguir lista os objetos de script que exigem caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="a7de1-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7de1-134">Objeto de script</span><span class="sxs-lookup"><span data-stu-id="a7de1-134">Scripting object</span></span></th>
<th><span data-ttu-id="a7de1-135">Método</span><span class="sxs-lookup"><span data-stu-id="a7de1-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7de1-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="a7de1-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="a7de1-138">[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="a7de1-139">[<strong>Excluir</strong>] (swbemservices-delete.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="a7de1-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="a7de1-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="a7de1-142">[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="a7de1-143">[<strong>Obter</strong>] (swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="a7de1-144">[<strong>Getasync</strong>] (swbemservices-getasync.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="a7de1-145">[<strong>ReferenceTo</strong>] (swbemservices-referencesto.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="a7de1-146">[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)</span><span class="sxs-lookup"><span data-stu-id="a7de1-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7de1-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="a7de1-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7de1-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
