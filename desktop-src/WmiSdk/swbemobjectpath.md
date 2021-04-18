---
description: Use os métodos e as propriedades do objeto SWbemObjectPath para construir e validar um caminho de objeto. Esse objeto pode ser criado pela chamada do VBScript CreateObject.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objeto SWbemObjectPath (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784536"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="942a2-104">Objeto SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="942a2-104">SWbemObjectPath object</span></span>

<span data-ttu-id="942a2-105">Use os métodos e as propriedades do objeto **SWbemObjectPath** para construir e validar um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="942a2-106">Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="942a2-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="942a2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="942a2-107">Members</span></span>

<span data-ttu-id="942a2-108">O objeto **SWbemObjectPath** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="942a2-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="942a2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="942a2-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="942a2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="942a2-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="942a2-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="942a2-111">Methods</span></span>

<span data-ttu-id="942a2-112">O objeto **SWbemObjectPath** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="942a2-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="942a2-113">Método</span><span class="sxs-lookup"><span data-stu-id="942a2-113">Method</span></span>                                                   | <span data-ttu-id="942a2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="942a2-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="942a2-115">**SetAsClass**</span><span class="sxs-lookup"><span data-stu-id="942a2-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="942a2-116">Força o caminho para tratar de uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="942a2-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="942a2-117">**SetAsSingleton**</span><span class="sxs-lookup"><span data-stu-id="942a2-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="942a2-118">Força o caminho para endereçar uma instância WMI singleton.</span><span class="sxs-lookup"><span data-stu-id="942a2-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="942a2-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="942a2-119">Properties</span></span>

<span data-ttu-id="942a2-120">O objeto **SWbemObjectPath** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="942a2-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="942a2-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="942a2-121">Property</span></span>                                                              | <span data-ttu-id="942a2-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="942a2-122">Access type</span></span>           | <span data-ttu-id="942a2-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="942a2-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="942a2-124">**Authority**</span><span class="sxs-lookup"><span data-stu-id="942a2-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="942a2-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-125">Read/write</span></span><br/> | <span data-ttu-id="942a2-126">Cadeia de caracteres que define o componente de autoridade do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="942a2-127">**Classe**</span><span class="sxs-lookup"><span data-stu-id="942a2-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="942a2-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-128">Read/write</span></span><br/> | <span data-ttu-id="942a2-129">Nome da classe que faz parte do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="942a2-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="942a2-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="942a2-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-131">Read/write</span></span><br/> | <span data-ttu-id="942a2-132">Cadeia de caracteres que contém o caminho em um formulário que pode ser usado como um nome de exibição de moniker.</span><span class="sxs-lookup"><span data-stu-id="942a2-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="942a2-133">Consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="942a2-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="942a2-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="942a2-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="942a2-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="942a2-135">Read-only</span></span><br/>  | <span data-ttu-id="942a2-136">Valor booliano que indica se esse caminho representa uma classe.</span><span class="sxs-lookup"><span data-stu-id="942a2-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="942a2-137">Isso é análogo à propriedade [ \_ \_ genus](wmi-system-properties.md) na API com.</span><span class="sxs-lookup"><span data-stu-id="942a2-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="942a2-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="942a2-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="942a2-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="942a2-139">Read-only</span></span><br/>  | <span data-ttu-id="942a2-140">Valor booliano que indica se esse caminho representa uma instância singleton.</span><span class="sxs-lookup"><span data-stu-id="942a2-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="942a2-141">**simétricas**</span><span class="sxs-lookup"><span data-stu-id="942a2-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="942a2-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="942a2-142">Read-only</span></span><br/>  | <span data-ttu-id="942a2-143">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contém as associações de valor de chave.</span><span class="sxs-lookup"><span data-stu-id="942a2-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="942a2-144">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="942a2-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="942a2-145">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-145">Read/write</span></span><br/> | <span data-ttu-id="942a2-146">Cadeia de caracteres que contém a localidade deste caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="942a2-147">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="942a2-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="942a2-148">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-148">Read/write</span></span><br/> | <span data-ttu-id="942a2-149">Nome do namespace que faz parte do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="942a2-150">Isso é o mesmo que a propriedade [ \_ \_ namespace](wmi-system-properties.md) na API com.</span><span class="sxs-lookup"><span data-stu-id="942a2-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="942a2-151">**ParentNamespace**</span><span class="sxs-lookup"><span data-stu-id="942a2-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="942a2-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="942a2-152">Read-only</span></span><br/>  | <span data-ttu-id="942a2-153">Nome do pai do namespace que faz parte do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="942a2-154">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="942a2-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="942a2-155">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-155">Read/write</span></span><br/> | <span data-ttu-id="942a2-156">Contém o caminho absoluto.</span><span class="sxs-lookup"><span data-stu-id="942a2-156">Contains the absolute path.</span></span> <span data-ttu-id="942a2-157">Isso é o mesmo que a propriedade do sistema [ \_ \_ Path](wmi-system-properties.md) na API com.</span><span class="sxs-lookup"><span data-stu-id="942a2-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="942a2-158">Essa é a propriedade padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="942a2-159">**Relpath**</span><span class="sxs-lookup"><span data-stu-id="942a2-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="942a2-160">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-160">Read/write</span></span><br/> | <span data-ttu-id="942a2-161">Contém o caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="942a2-161">Contains the relative path.</span></span> <span data-ttu-id="942a2-162">Isso é o mesmo que a propriedade do sistema [ \_ \_ RelPath](wmi-system-properties.md) na API com.</span><span class="sxs-lookup"><span data-stu-id="942a2-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="942a2-163">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="942a2-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="942a2-164">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="942a2-164">Read-only</span></span><br/>  | <span data-ttu-id="942a2-165">Usado para ler ou alterar as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="942a2-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="942a2-166">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="942a2-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="942a2-167">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="942a2-167">Read/write</span></span><br/> | <span data-ttu-id="942a2-168">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="942a2-168">Name of the server.</span></span> <span data-ttu-id="942a2-169">Isso é o mesmo que a propriedade do sistema de [ \_ \_ servidor](wmi-system-properties.md) na API com.</span><span class="sxs-lookup"><span data-stu-id="942a2-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="942a2-170">Exemplos</span><span class="sxs-lookup"><span data-stu-id="942a2-170">Examples</span></span>

<span data-ttu-id="942a2-171">O exemplo de código VBScript a seguir demonstra como criar caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="942a2-172">O exemplo de código Perl a seguir demonstra como criar caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="942a2-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="942a2-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="942a2-173">Requirements</span></span>



| <span data-ttu-id="942a2-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="942a2-174">Requirement</span></span> | <span data-ttu-id="942a2-175">Valor</span><span class="sxs-lookup"><span data-stu-id="942a2-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="942a2-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="942a2-176">Minimum supported client</span></span><br/> | <span data-ttu-id="942a2-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="942a2-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="942a2-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="942a2-178">Minimum supported server</span></span><br/> | <span data-ttu-id="942a2-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="942a2-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="942a2-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="942a2-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="942a2-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="942a2-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="942a2-182">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="942a2-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="942a2-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="942a2-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="942a2-184">DLL</span><span class="sxs-lookup"><span data-stu-id="942a2-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="942a2-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="942a2-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="942a2-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="942a2-186">CLSID</span></span><br/>                    | <span data-ttu-id="942a2-187">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="942a2-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="942a2-188">IID</span><span class="sxs-lookup"><span data-stu-id="942a2-188">IID</span></span><br/>                      | <span data-ttu-id="942a2-189">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="942a2-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="942a2-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="942a2-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942a2-191">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="942a2-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




