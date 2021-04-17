---
description: Um objeto SWbemNamedValueSet é uma coleção de objetos SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objeto SWbemNamedValueSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761527"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="395dd-103">Objeto SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="395dd-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="395dd-104">Um objeto **SWbemNamedValueSet** é uma coleção de objetos [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="395dd-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="395dd-105">Os métodos e as propriedades de **SWbemNamedValueSet** são usados principalmente para enviar mais informações aos provedores ao enviar determinadas chamadas para o WMI.</span><span class="sxs-lookup"><span data-stu-id="395dd-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="395dd-106">Todas as chamadas em [**SWbemServices**](swbemservices.md)e algumas chamadas em [**SWbemObject**](swbemobject.md), usam um parâmetro opcional que é um objeto desse tipo.</span><span class="sxs-lookup"><span data-stu-id="395dd-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="395dd-107">Um cliente pode adicionar informações a um objeto **SWbemNamedValueSet** e enviar o objeto **SWbemNamedValueSet** com a chamada como um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="395dd-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="395dd-108">Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="395dd-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="395dd-109">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="395dd-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="395dd-110">Importante-se possível, não use esse mecanismo porque ele pode interromper o modelo de acesso uniforme que é a base do WMI.</span><span class="sxs-lookup"><span data-stu-id="395dd-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="395dd-111">Se um provedor usar esse mecanismo, é importante que esse mecanismo seja usado da maneira mais moderada possível.</span><span class="sxs-lookup"><span data-stu-id="395dd-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="395dd-112">Se um provedor exigir uma grande quantidade de informações de contexto altamente específicas para responder a uma solicitação, todos os clientes deverão ser codificados para fornecer essas informações.</span><span class="sxs-lookup"><span data-stu-id="395dd-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="395dd-113">Esse mecanismo permite que você acesse provedores, se necessário.</span><span class="sxs-lookup"><span data-stu-id="395dd-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="395dd-114">Um objeto **SWbemNamedValueSet** é uma coleção de elementos [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="395dd-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="395dd-115">Esses itens são adicionados à coleção usando o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="395dd-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="395dd-116">Eles são removidos usando o método [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) e recuperados usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="395dd-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="395dd-117">Você pode acessar os métodos para preencher qualquer informação de contexto exigida por um provedor dinâmico.</span><span class="sxs-lookup"><span data-stu-id="395dd-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="395dd-118">Depois de chamar um dos métodos [**SWbemServices**](swbemservices.md) , você pode reutilizar o objeto **SWbemNamedValueSet** para outra chamada.</span><span class="sxs-lookup"><span data-stu-id="395dd-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="395dd-119">O provedor subjacente determina as informações contidas em um objeto **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="395dd-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="395dd-120">O WMI não faz uso das informações, mas simplesmente a encaminha para o provedor.</span><span class="sxs-lookup"><span data-stu-id="395dd-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="395dd-121">Os provedores devem publicar as informações de contexto necessárias para atender a solicitações.</span><span class="sxs-lookup"><span data-stu-id="395dd-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="395dd-122">Membros</span><span class="sxs-lookup"><span data-stu-id="395dd-122">Members</span></span>

<span data-ttu-id="395dd-123">O objeto **SWbemNamedValueSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="395dd-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="395dd-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="395dd-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="395dd-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="395dd-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="395dd-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="395dd-126">Methods</span></span>

<span data-ttu-id="395dd-127">O objeto **SWbemNamedValueSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="395dd-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="395dd-128">Método</span><span class="sxs-lookup"><span data-stu-id="395dd-128">Method</span></span>                                            | <span data-ttu-id="395dd-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="395dd-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395dd-130">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="395dd-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="395dd-131">Adiciona um objeto [**SWbemNamedValue**](swbemnamedvalue.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="395dd-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="395dd-132">**8i**</span><span class="sxs-lookup"><span data-stu-id="395dd-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="395dd-133">Faz uma cópia desta coleção **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="395dd-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="395dd-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="395dd-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="395dd-135">Remove todos os itens da coleção, tornando o objeto **SWbemNamedValueSet** vazio.</span><span class="sxs-lookup"><span data-stu-id="395dd-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="395dd-136">**Item**</span><span class="sxs-lookup"><span data-stu-id="395dd-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="395dd-137">Recupera um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="395dd-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="395dd-138">Esse é o método padrão do objeto.</span><span class="sxs-lookup"><span data-stu-id="395dd-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="395dd-139">**Remover**</span><span class="sxs-lookup"><span data-stu-id="395dd-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="395dd-140">Remove um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="395dd-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="395dd-141">Propriedades</span><span class="sxs-lookup"><span data-stu-id="395dd-141">Properties</span></span>

<span data-ttu-id="395dd-142">O objeto **SWbemNamedValueSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="395dd-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="395dd-143">Propriedade</span><span class="sxs-lookup"><span data-stu-id="395dd-143">Property</span></span>                                             | <span data-ttu-id="395dd-144">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="395dd-144">Access type</span></span>          | <span data-ttu-id="395dd-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="395dd-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="395dd-146">**Contar**</span><span class="sxs-lookup"><span data-stu-id="395dd-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="395dd-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="395dd-147">Read-only</span></span><br/> | <span data-ttu-id="395dd-148">Número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="395dd-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="395dd-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="395dd-149">Examples</span></span>

<span data-ttu-id="395dd-150">O exemplo de VBScript a seguir demonstra a manipulação de conjuntos de valores nomeados, no caso de o valor nomeado ser um tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="395dd-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="395dd-151">O exemplo do Perl a seguir demonstra a manipulação de conjuntos de valores nomeados, no caso de o valor nomeado ser um tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="395dd-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="395dd-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="395dd-152">Requirements</span></span>



| <span data-ttu-id="395dd-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="395dd-153">Requirement</span></span> | <span data-ttu-id="395dd-154">Valor</span><span class="sxs-lookup"><span data-stu-id="395dd-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="395dd-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="395dd-155">Minimum supported client</span></span><br/> | <span data-ttu-id="395dd-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="395dd-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="395dd-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="395dd-157">Minimum supported server</span></span><br/> | <span data-ttu-id="395dd-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="395dd-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="395dd-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="395dd-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="395dd-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="395dd-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="395dd-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="395dd-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="395dd-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="395dd-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="395dd-163">DLL</span><span class="sxs-lookup"><span data-stu-id="395dd-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="395dd-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395dd-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="395dd-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="395dd-165">CLSID</span></span><br/>                    | <span data-ttu-id="395dd-166">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="395dd-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="395dd-167">IID</span><span class="sxs-lookup"><span data-stu-id="395dd-167">IID</span></span><br/>                      | <span data-ttu-id="395dd-168">ISWbemNamedValueSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="395dd-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="395dd-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="395dd-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395dd-170">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="395dd-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




