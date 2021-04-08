---
title: Objeto Enumerator (WSManDisp. h)
description: Representa um fluxo de resultados retornados de operações, como uma operação de pull.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Objeto de enumerador Gerenciamento Remoto do Windows
- Objeto Enumerator Gerenciamento Remoto do Windows, descrito
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009686"
---
# <a name="enumerator-object"></a><span data-ttu-id="e242e-105">Objeto Enumerator</span><span class="sxs-lookup"><span data-stu-id="e242e-105">Enumerator object</span></span>

<span data-ttu-id="e242e-106">Representa um fluxo de resultados retornados de operações, como uma operação de pull.</span><span class="sxs-lookup"><span data-stu-id="e242e-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="e242e-107">Por exemplo, o método [**Session. enumerar**](session-enumerate.md) retorna vários resultados.</span><span class="sxs-lookup"><span data-stu-id="e242e-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="e242e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e242e-108">Members</span></span>

<span data-ttu-id="e242e-109">O objeto **Enumerator** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e242e-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="e242e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e242e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e242e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e242e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e242e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e242e-112">Methods</span></span>

<span data-ttu-id="e242e-113">O objeto **Enumerator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e242e-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="e242e-114">Método</span><span class="sxs-lookup"><span data-stu-id="e242e-114">Method</span></span>                                  | <span data-ttu-id="e242e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e242e-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e242e-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="e242e-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="e242e-117">Recupera um item do recurso e retorna uma representação XML do item.</span><span class="sxs-lookup"><span data-stu-id="e242e-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e242e-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e242e-118">Properties</span></span>

<span data-ttu-id="e242e-119">O objeto **Enumerator** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e242e-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="e242e-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e242e-120">Property</span></span>                                                     | <span data-ttu-id="e242e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e242e-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e242e-122">**AtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="e242e-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="e242e-123">Obtém um valor booliano que indica se há mais itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="e242e-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="e242e-124">**Erro**</span><span class="sxs-lookup"><span data-stu-id="e242e-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="e242e-125">Obtém uma representação XML de informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="e242e-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e242e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e242e-126">Remarks</span></span>

<span data-ttu-id="e242e-127">Para iniciar uma enumeração, use [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="e242e-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="e242e-128">Para fazer uma operação [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) que continua lendo itens na enumeração, use [**Enumerator. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="e242e-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="e242e-129">O objeto **enumerador** corresponde à interface [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .</span><span class="sxs-lookup"><span data-stu-id="e242e-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="e242e-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e242e-130">Examples</span></span>

<span data-ttu-id="e242e-131">O exemplo de código VBScript a seguir enumera todos os discos em um computador remoto especificado pelo nome de domínio totalmente qualificado (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="e242e-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="e242e-132">A sub-rotina DisplayOutput formata a saída de dados da mesma maneira que a ferramenta WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="e242e-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="e242e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e242e-133">Requirements</span></span>



| <span data-ttu-id="e242e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e242e-134">Requirement</span></span> | <span data-ttu-id="e242e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e242e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e242e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e242e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e242e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e242e-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e242e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e242e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e242e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e242e-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e242e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e242e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e242e-141"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e242e-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e242e-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="e242e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e242e-143"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e242e-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e242e-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e242e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="e242e-145"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e242e-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e242e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e242e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e242e-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e242e-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e242e-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="e242e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e242e-149">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="e242e-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="e242e-150">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="e242e-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="e242e-151">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="e242e-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





