---
description: Um objeto SWbemObjectSet é uma coleção de objetos SWbemObject. Para obter mais informações, consulte Acessando uma coleção. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objeto SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171782"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="42228-105">Objeto SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="42228-105">SWbemObjectSet object</span></span>

<span data-ttu-id="42228-106">Um objeto **SWbemObjectSet** é uma coleção de objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="42228-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="42228-107">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="42228-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="42228-108">Este objeto não pode ser criado pela chamada VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="42228-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="42228-109">Você pode obter um objeto **SWbemObjectSet** chamando qualquer um dos seguintes métodos ou seus equivalentes assíncronos:</span><span class="sxs-lookup"><span data-stu-id="42228-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="42228-110">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="42228-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="42228-111">**SWbemObject. instâncias\_**</span><span class="sxs-lookup"><span data-stu-id="42228-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="42228-112">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="42228-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="42228-113">**Subclasses de SWbemObject\_**</span><span class="sxs-lookup"><span data-stu-id="42228-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="42228-114">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="42228-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="42228-115">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="42228-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="42228-116">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="42228-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="42228-117">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="42228-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="42228-118">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="42228-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="42228-119">O objeto **SWbemObjectSet** não dá suporte aos métodos opcionais **Add** e **Remove** Collection.</span><span class="sxs-lookup"><span data-stu-id="42228-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="42228-120">Como o retorno de chamada para o coletor não pode ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="42228-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="42228-121">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42228-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="42228-122">Membros</span><span class="sxs-lookup"><span data-stu-id="42228-122">Members</span></span>

<span data-ttu-id="42228-123">O objeto **SWbemObjectSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="42228-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="42228-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="42228-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="42228-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42228-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42228-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="42228-126">Methods</span></span>

<span data-ttu-id="42228-127">O objeto **SWbemObjectSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="42228-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="42228-128">Método</span><span class="sxs-lookup"><span data-stu-id="42228-128">Method</span></span>                              | <span data-ttu-id="42228-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="42228-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42228-130">**Item**</span><span class="sxs-lookup"><span data-stu-id="42228-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="42228-131">Recupera um objeto [**SWbemObject**](swbemobject.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="42228-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="42228-132">Esse é o método padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="42228-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42228-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42228-133">Properties</span></span>

<span data-ttu-id="42228-134">O objeto **SWbemObjectSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="42228-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="42228-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="42228-135">Property</span></span>                                                  | <span data-ttu-id="42228-136">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="42228-136">Access type</span></span>          | <span data-ttu-id="42228-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="42228-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="42228-138">**Contar**</span><span class="sxs-lookup"><span data-stu-id="42228-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="42228-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42228-139">Read-only</span></span><br/> | <span data-ttu-id="42228-140">Número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="42228-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="42228-141">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="42228-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="42228-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42228-142">Read-only</span></span><br/> | <span data-ttu-id="42228-143">Usado para ler ou alterar as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="42228-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42228-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="42228-144">Remarks</span></span>

<span data-ttu-id="42228-145">Um **SWbemObjectSet** é uma coleção de zero ou mais objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="42228-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="42228-146">Cada **SWbemObject** em um **SWbemObjectSet** pode representar uma das duas coisas:</span><span class="sxs-lookup"><span data-stu-id="42228-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="42228-147">Uma instância de um recurso gerenciado por WMI.</span><span class="sxs-lookup"><span data-stu-id="42228-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="42228-148">Uma instância de uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="42228-148">An instance of a class definition.</span></span>

<span data-ttu-id="42228-149">O uso mais comum dessa classe no WMI é como o valor de retorno para uma chamada [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) ou [**InstancesOf**](swbemservices-instancesof.md) , conforme descrito no exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="42228-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="42228-150">Na maior parte, a única coisa que você fará com um **SWbemObjectSet** é enumerar todos os objetos contidos na coleção em si.</span><span class="sxs-lookup"><span data-stu-id="42228-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="42228-151">No entanto, o **SWbemObjectSet** inclui uma contagem de propriedades que pode ser útil no script de administração do sistema.</span><span class="sxs-lookup"><span data-stu-id="42228-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="42228-152">Como o nome implica, Count informa o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="42228-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="42228-153">Por exemplo, esse script recupera uma coleção de todos os serviços instalados em um computador e, em seguida, ecoa o número total de serviços encontrados:</span><span class="sxs-lookup"><span data-stu-id="42228-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="42228-154">Para obter mais informações sobre como usar essa classe, consulte [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="42228-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="42228-155">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42228-155">Examples</span></span>

<span data-ttu-id="42228-156">O exemplo de código VBScript a seguir ilustra como as coleções **SWbemObjectSet** são manipuladas.</span><span class="sxs-lookup"><span data-stu-id="42228-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="42228-157">O exemplo de código Perl a seguir ilustra como as coleções de **SWbemObjectSet** são manipuladas.</span><span class="sxs-lookup"><span data-stu-id="42228-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="42228-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42228-158">Requirements</span></span>



| <span data-ttu-id="42228-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="42228-159">Requirement</span></span> | <span data-ttu-id="42228-160">Valor</span><span class="sxs-lookup"><span data-stu-id="42228-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42228-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42228-161">Minimum supported client</span></span><br/> | <span data-ttu-id="42228-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42228-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42228-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42228-163">Minimum supported server</span></span><br/> | <span data-ttu-id="42228-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42228-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42228-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42228-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="42228-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42228-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42228-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="42228-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="42228-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42228-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42228-169">DLL</span><span class="sxs-lookup"><span data-stu-id="42228-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42228-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42228-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42228-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="42228-171">CLSID</span></span><br/>                    | <span data-ttu-id="42228-172">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="42228-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="42228-173">IID</span><span class="sxs-lookup"><span data-stu-id="42228-173">IID</span></span><br/>                      | <span data-ttu-id="42228-174">ISWbemObjectSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="42228-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="42228-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="42228-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42228-176">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="42228-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




