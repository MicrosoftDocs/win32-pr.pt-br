---
title: Método Session. put (WSManDisp. h)
description: Atualiza um recurso.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Put
- Método Put Gerenciamento Remoto do Windows, objeto Session
- Objeto de sessão Gerenciamento Remoto do Windows, método Put
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369761"
---
# <a name="sessionput-method"></a><span data-ttu-id="2f97b-106">Método Session. put</span><span class="sxs-lookup"><span data-stu-id="2f97b-106">Session.Put method</span></span>

<span data-ttu-id="2f97b-107">Atualiza um recurso.</span><span class="sxs-lookup"><span data-stu-id="2f97b-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f97b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f97b-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f97b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f97b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f97b-110">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f97b-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f97b-111">O identificador do recurso a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="2f97b-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="2f97b-112">Esse parâmetro pode conter um dos elementos contidos na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="2f97b-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="2f97b-113">URI com ou sem [*seletores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="2f97b-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="2f97b-114">Ao chamar o método **Put** para obter um recurso WMI, use a propriedade de chave ou as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="2f97b-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="2f97b-115">Por exemplo, no exemplo de código a seguir Visual Basic Scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="2f97b-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="2f97b-116">Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="2f97b-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="2f97b-117">Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="2f97b-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="2f97b-118">Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="2f97b-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="2f97b-119">*recurso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2f97b-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f97b-120">O conteúdo do recurso atualizado.</span><span class="sxs-lookup"><span data-stu-id="2f97b-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="2f97b-121">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2f97b-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f97b-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="2f97b-122">Reserved.</span></span> <span data-ttu-id="2f97b-123">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2f97b-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f97b-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f97b-124">Return value</span></span>

<span data-ttu-id="2f97b-125">O XML que contém o conteúdo do recurso atualizado.</span><span class="sxs-lookup"><span data-stu-id="2f97b-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="2f97b-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f97b-126">Examples</span></span>

<span data-ttu-id="2f97b-127">O exemplo de código VBScript a seguir grava dados no objeto [**\_ WMISetting do Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) .</span><span class="sxs-lookup"><span data-stu-id="2f97b-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="2f97b-128">Você deve incluir todas as propriedades que não sejam da matriz do objeto no XML do parâmetro de *recurso* .</span><span class="sxs-lookup"><span data-stu-id="2f97b-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="2f97b-129">A ordem das propriedades não é significativa.</span><span class="sxs-lookup"><span data-stu-id="2f97b-129">The order of the properties is not significant.</span></span>


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2f97b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f97b-130">Requirements</span></span>



| <span data-ttu-id="2f97b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f97b-131">Requirement</span></span> | <span data-ttu-id="2f97b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2f97b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f97b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f97b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2f97b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f97b-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2f97b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f97b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2f97b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f97b-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2f97b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f97b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f97b-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f97b-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f97b-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="2f97b-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f97b-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f97b-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f97b-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f97b-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f97b-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f97b-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f97b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f97b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f97b-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f97b-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f97b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f97b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f97b-146">**Session**</span><span class="sxs-lookup"><span data-stu-id="2f97b-146">**Session**</span></span>](session.md)
</dt> </dl>

 

