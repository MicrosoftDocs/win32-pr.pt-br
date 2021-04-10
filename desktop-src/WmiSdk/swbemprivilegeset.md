---
description: Um objeto SWbemPrivilegeSet é uma coleção de objetos SWbemPrivilege em um objeto SWbemSecurity que solicita privilégios específicos para um objeto Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objeto SWbemPrivilegeSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296593"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="b9f2f-103">Objeto SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="b9f2f-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="b9f2f-104">Um objeto **SWbemPrivilegeSet** é uma coleção de objetos [**SWbemPrivilege**](swbemprivilege.md) em um objeto [**SWbemSecurity**](swbemsecurity.md) que solicita privilégios específicos para um objeto Instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b9f2f-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="b9f2f-105">Consulte a lista de privilégios em [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b9f2f-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="b9f2f-106">Os itens são adicionados à coleção usando os métodos [**Add**](swbemprivilegeset-add.md) e [**AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f2f-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="b9f2f-107">Os itens são recuperados da coleção usando o método [**Item**](swbemprivilegeset-item.md) e removidos usando o método [**Remove**](swbemprivilegeset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f2f-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="b9f2f-108">Este objeto não pode ser criado pela chamada do método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) do VBScript.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="b9f2f-109">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="b9f2f-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="b9f2f-110">Um objeto **SWbemPrivilegeSet** é um conjunto de solicitações de substituição de privilégio para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="b9f2f-111">Quando uma chamada à API é feita usando esse objeto, as solicitações de substituição de privilégio são tentadas.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="b9f2f-112">O objeto **SWbemPrivilegeSet** não define os privilégios disponíveis para o usuário ou processo atual.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="b9f2f-113">Em outras palavras, a obtenção de privilégios para qualquer objeto WMI não identifica as configurações de privilégio feitas na conexão com o WMI ou os privilégios em vigor quando um objeto é entregue a um coletor.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="b9f2f-114">Membros</span><span class="sxs-lookup"><span data-stu-id="b9f2f-114">Members</span></span>

<span data-ttu-id="b9f2f-115">O objeto **SWbemPrivilegeSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b9f2f-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="b9f2f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9f2f-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9f2f-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9f2f-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9f2f-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9f2f-118">Methods</span></span>

<span data-ttu-id="b9f2f-119">O objeto **SWbemPrivilegeSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="b9f2f-120">Método</span><span class="sxs-lookup"><span data-stu-id="b9f2f-120">Method</span></span>                                               | <span data-ttu-id="b9f2f-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9f2f-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9f2f-122">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="b9f2f-123">Adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** usando uma constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="b9f2f-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="b9f2f-124">**AddAsString**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="b9f2f-125">Adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** usando uma cadeia de caracteres de privilégio.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="b9f2f-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="b9f2f-127">Exclui todos os privilégios da coleção.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="b9f2f-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="b9f2f-129">Recupera um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="b9f2f-130">Esse é o método padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="b9f2f-131">**Remover**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="b9f2f-132">Remove um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="b9f2f-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9f2f-133">Properties</span></span>

<span data-ttu-id="b9f2f-134">O objeto **SWbemPrivilegeSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="b9f2f-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b9f2f-135">Property</span></span>                                            | <span data-ttu-id="b9f2f-136">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b9f2f-136">Access type</span></span>          | <span data-ttu-id="b9f2f-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9f2f-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="b9f2f-138">**Contar**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="b9f2f-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9f2f-139">Read-only</span></span><br/> | <span data-ttu-id="b9f2f-140">Número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="b9f2f-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="b9f2f-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9f2f-141">Examples</span></span>

<span data-ttu-id="b9f2f-142">O exemplo de código VBScript a seguir obtém um objeto SWbemPrivileges e adiciona todos os privilégios disponíveis à coleção por valor de privilégio, conforme definido em [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="b9f2f-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="b9f2f-143">O exemplo de código VBScript a seguir demonstra como adicionar privilégios usando o objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="b9f2f-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="b9f2f-144">O exemplo de código do Perl a seguir demonstra como adicionar privilégios usando o objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="b9f2f-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="b9f2f-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9f2f-145">Requirements</span></span>



| <span data-ttu-id="b9f2f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9f2f-146">Requirement</span></span> | <span data-ttu-id="b9f2f-147">Valor</span><span class="sxs-lookup"><span data-stu-id="b9f2f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f2f-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f2f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f2f-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9f2f-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9f2f-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f2f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f2f-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f2f-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9f2f-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9f2f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9f2f-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9f2f-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9f2f-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b9f2f-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9f2f-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9f2f-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9f2f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b9f2f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9f2f-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9f2f-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9f2f-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="b9f2f-158">CLSID</span></span><br/>                    | <span data-ttu-id="b9f2f-159">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="b9f2f-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="b9f2f-160">IID</span><span class="sxs-lookup"><span data-stu-id="b9f2f-160">IID</span></span><br/>                      | <span data-ttu-id="b9f2f-161">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="b9f2f-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="b9f2f-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9f2f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f2f-163">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="b9f2f-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="b9f2f-164">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="b9f2f-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="b9f2f-165">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="b9f2f-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="b9f2f-166">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="b9f2f-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="b9f2f-167">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="b9f2f-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

