---
title: Objeto ResourceLocator (WSManDisp. h)
description: Fornece o caminho para um recurso. Você pode usar um objeto ResourceLocator em vez de um URI de recurso em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de objeto ResourceLocator
- Gerenciamento Remoto do Windows de objeto ResourceLocator, descrito
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085262"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="a47fc-106">Objeto ResourceLocator</span><span class="sxs-lookup"><span data-stu-id="a47fc-106">ResourceLocator object</span></span>

<span data-ttu-id="a47fc-107">Um objeto que fornece o caminho para um recurso.</span><span class="sxs-lookup"><span data-stu-id="a47fc-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="a47fc-108">Você pode usar um objeto **ResourceLocator** em vez de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="a47fc-109">Este objeto permite que você:</span><span class="sxs-lookup"><span data-stu-id="a47fc-109">This object enables you to:</span></span>

-   <span data-ttu-id="a47fc-110">Adicione um ou mais [*seletores*](windows-remote-management-glossary.md) que identificam uma instância específica de um recurso.</span><span class="sxs-lookup"><span data-stu-id="a47fc-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="a47fc-111">Isso é o mesmo que fornecer um valor de chave no URI de recurso para um recurso que usa chaves.</span><span class="sxs-lookup"><span data-stu-id="a47fc-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="a47fc-112">Para obter mais informações, consulte [**ResourceLocator. Addseletor**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="a47fc-113">Você pode fazer uma operação semelhante usando o parâmetro *Filter* em uma chamada para [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="a47fc-114">Especifique um caminho de [*fragmento*](windows-remote-management-glossary.md) e um dialeto para obter apenas uma propriedade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="a47fc-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="a47fc-115">Você também pode especificar um ou todos os elementos de uma propriedade de matriz fornecendo o índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="a47fc-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="a47fc-116">Para obter mais informações, consulte [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="a47fc-117">Adicione uma ou mais [*Opções*](windows-remote-management-glossary.md) que uma fonte de dados pode exigir para processar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a47fc-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="a47fc-118">Para obter mais informações, consulte [**ResourceLocator. AddOption**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="a47fc-119">Para obter mais informações, consulte [consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="a47fc-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="a47fc-120">Membros</span><span class="sxs-lookup"><span data-stu-id="a47fc-120">Members</span></span>

<span data-ttu-id="a47fc-121">O objeto **ResourceLocator** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a47fc-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="a47fc-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="a47fc-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="a47fc-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a47fc-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a47fc-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="a47fc-124">Methods</span></span>

<span data-ttu-id="a47fc-125">O objeto **ResourceLocator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a47fc-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="a47fc-126">Método</span><span class="sxs-lookup"><span data-stu-id="a47fc-126">Method</span></span>                                                   | <span data-ttu-id="a47fc-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="a47fc-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a47fc-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="a47fc-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="a47fc-129">Adiciona dados adicionais necessários para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a47fc-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="a47fc-130">**Addseletor**</span><span class="sxs-lookup"><span data-stu-id="a47fc-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="a47fc-131">Adiciona um [*seletor*](windows-remote-management-glossary.md) ao objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="a47fc-132">**Clearoptions**</span><span class="sxs-lookup"><span data-stu-id="a47fc-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="a47fc-133">Remove todas [*as opções*](windows-remote-management-glossary.md) do objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="a47fc-134">**ClearSelectors**</span><span class="sxs-lookup"><span data-stu-id="a47fc-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="a47fc-135">Remove todos os seletores de um objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="a47fc-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a47fc-136">Properties</span></span>

<span data-ttu-id="a47fc-137">O objeto **ResourceLocator** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a47fc-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="a47fc-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a47fc-138">Property</span></span>                                                                          | <span data-ttu-id="a47fc-139">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="a47fc-139">Access type</span></span>           | <span data-ttu-id="a47fc-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="a47fc-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a47fc-141">**FragmentDialect**</span><span class="sxs-lookup"><span data-stu-id="a47fc-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="a47fc-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a47fc-142">Read/write</span></span><br/> | <span data-ttu-id="a47fc-143">Obtém ou define o dialeto de idioma para um [*fragmento*](windows-remote-management-glossary.md)de [*recurso*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a47fc-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="a47fc-144">**FragmentPath**</span><span class="sxs-lookup"><span data-stu-id="a47fc-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="a47fc-145">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a47fc-145">Read/write</span></span><br/> | <span data-ttu-id="a47fc-146">Obtém ou define o caminho para um [](windows-remote-management-glossary.md) [*fragmento*](windows-remote-management-glossary.md) de recurso ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="a47fc-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="a47fc-147">**MustUnderstandoptions**</span><span class="sxs-lookup"><span data-stu-id="a47fc-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="a47fc-148">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a47fc-148">Read/write</span></span><br/> | <span data-ttu-id="a47fc-149">Obtém ou define o valor **mustunderstandoptions** para o objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a47fc-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="a47fc-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="a47fc-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a47fc-151">Read/write</span></span><br/> | <span data-ttu-id="a47fc-152">Obtém ou define o [*URI do recurso*](windows-remote-management-glossary.md) em um objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a47fc-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="a47fc-153">Remarks</span></span>

<span data-ttu-id="a47fc-154">O objeto **ResourceLocator** corresponde à interface **IWSManResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="a47fc-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="a47fc-155">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a47fc-155">Examples</span></span>

<span data-ttu-id="a47fc-156">O exemplo de código VBScript a seguir obtém as propriedades **NumberOfLogicalProcessors** e **NumberOfCores** de uma instância específica [**do \_ processador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="a47fc-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a47fc-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a47fc-157">Requirements</span></span>



| <span data-ttu-id="a47fc-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="a47fc-158">Requirement</span></span> | <span data-ttu-id="a47fc-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a47fc-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47fc-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a47fc-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a47fc-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a47fc-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a47fc-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a47fc-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a47fc-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a47fc-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a47fc-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a47fc-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="a47fc-165"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a47fc-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a47fc-166">INSERI</span><span class="sxs-lookup"><span data-stu-id="a47fc-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a47fc-167"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a47fc-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a47fc-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a47fc-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="a47fc-169"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a47fc-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a47fc-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a47fc-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a47fc-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a47fc-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a47fc-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="a47fc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a47fc-173">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="a47fc-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

