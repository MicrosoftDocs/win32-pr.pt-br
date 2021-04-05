---
title: Método Session. Invoke (WSManDisp. h)
description: Invoca um método e retorna resultados da chamada de método.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Invoke
- Método Invoke Gerenciamento Remoto do Windows, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, método Invoke
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645080"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="50af7-106">Método Session. Invoke</span><span class="sxs-lookup"><span data-stu-id="50af7-106">Session.Invoke method</span></span>

<span data-ttu-id="50af7-107">Invoca um método e retorna resultados da chamada de método.</span><span class="sxs-lookup"><span data-stu-id="50af7-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="50af7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50af7-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50af7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50af7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50af7-110">*actionUri* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50af7-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50af7-111">O URI do método a ser invocado.</span><span class="sxs-lookup"><span data-stu-id="50af7-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="50af7-112">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50af7-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50af7-113">O identificador do recurso a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="50af7-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="50af7-114">Esse parâmetro pode conter um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="50af7-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="50af7-115">URI com ou sem [*seletores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="50af7-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="50af7-116">No exemplo a seguir Visual Basic Scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="50af7-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="50af7-117">Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="50af7-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="50af7-118">Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="50af7-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="50af7-119">Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="50af7-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="50af7-120">*parâmetros* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="50af7-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50af7-121">A representação XML da entrada para o método.</span><span class="sxs-lookup"><span data-stu-id="50af7-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="50af7-122">Essa cadeia de caracteres deve ser fornecida, ou esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="50af7-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="50af7-123">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50af7-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50af7-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="50af7-124">Reserved.</span></span> <span data-ttu-id="50af7-125">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="50af7-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50af7-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50af7-126">Return value</span></span>

<span data-ttu-id="50af7-127">A representação XML da saída do método.</span><span class="sxs-lookup"><span data-stu-id="50af7-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="50af7-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50af7-128">Examples</span></span>

<span data-ttu-id="50af7-129">O exemplo de código VBScript a seguir inicia um processo de Calc.exe.</span><span class="sxs-lookup"><span data-stu-id="50af7-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="50af7-130">O parâmetro *strInputParameters* contém os parâmetros de entrada no formato XML.</span><span class="sxs-lookup"><span data-stu-id="50af7-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="50af7-131">O único parâmetro de entrada necessário para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe [**de \_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) é a linha de comando a ser executada.</span><span class="sxs-lookup"><span data-stu-id="50af7-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="50af7-132">O exemplo de código VBScript a seguir chama o método **Session. Invoke** para executar o método [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="50af7-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="50af7-133">O método **StopService** não tem parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="50af7-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="50af7-134">No entanto, o método **Invoke** requer uma cadeia de caracteres XML no parâmetro *Parameters* .</span><span class="sxs-lookup"><span data-stu-id="50af7-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="50af7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50af7-135">Requirements</span></span>



| <span data-ttu-id="50af7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="50af7-136">Requirement</span></span> | <span data-ttu-id="50af7-137">Valor</span><span class="sxs-lookup"><span data-stu-id="50af7-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50af7-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50af7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="50af7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50af7-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="50af7-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50af7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="50af7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50af7-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="50af7-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50af7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="50af7-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50af7-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50af7-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="50af7-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50af7-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50af7-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="50af7-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50af7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="50af7-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50af7-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50af7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="50af7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50af7-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50af7-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50af7-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="50af7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50af7-151">**Session**</span><span class="sxs-lookup"><span data-stu-id="50af7-151">**Session**</span></span>](session.md)
</dt> </dl>

 

