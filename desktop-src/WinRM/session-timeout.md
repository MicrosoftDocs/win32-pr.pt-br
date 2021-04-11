---
title: Propriedade Session. Timeout (WSManDisp. h)
description: Define e obtém a quantidade máxima de tempo, em milissegundos, que o aplicativo cliente aguarda Gerenciamento Remoto do Windows concluir suas operações.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da Propriedade Timeout
- Propriedade Timeout Gerenciamento Remoto do Windows, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, Propriedade Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295920"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="1824e-106">Propriedade Session. Timeout</span><span class="sxs-lookup"><span data-stu-id="1824e-106">Session.Timeout property</span></span>

<span data-ttu-id="1824e-107">Define e obtém a quantidade máxima de tempo, em milissegundos, que o aplicativo cliente aguarda Gerenciamento Remoto do Windows concluir suas operações.</span><span class="sxs-lookup"><span data-stu-id="1824e-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="1824e-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1824e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1824e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1824e-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="1824e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1824e-110">Property value</span></span>

<span data-ttu-id="1824e-111">Valor de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="1824e-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="1824e-112">Quando o valor de tempo limite for excedido, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1824e-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="1824e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1824e-113">Remarks</span></span>

<span data-ttu-id="1824e-114">O valor de tempo limite pode ser definido antes de cada operação executada pelo agente.</span><span class="sxs-lookup"><span data-stu-id="1824e-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="1824e-115">Se um valor de tempo limite não for especificado, o agente definirá o valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="1824e-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="1824e-116">Durante uma operação de enumeração, o valor de tempo limite não pode ser redefinido enquanto o recurso está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="1824e-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="1824e-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1824e-117">Examples</span></span>

<span data-ttu-id="1824e-118">O exemplo de código VBScript a seguir inicia um processo de Calc.exe usando o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe de [**\_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="1824e-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="1824e-119">O parâmetro *strInputParameters* contém os parâmetros de entrada no formato XML.</span><span class="sxs-lookup"><span data-stu-id="1824e-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="1824e-120">O script especifica um tempo limite para a sessão.</span><span class="sxs-lookup"><span data-stu-id="1824e-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="1824e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1824e-121">Requirements</span></span>



| <span data-ttu-id="1824e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1824e-122">Requirement</span></span> | <span data-ttu-id="1824e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1824e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1824e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1824e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1824e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1824e-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1824e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1824e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1824e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1824e-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1824e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1824e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1824e-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1824e-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1824e-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="1824e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1824e-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1824e-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1824e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1824e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1824e-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1824e-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1824e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1824e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1824e-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1824e-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1824e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1824e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1824e-137">**Session**</span><span class="sxs-lookup"><span data-stu-id="1824e-137">**Session**</span></span>](session.md)
</dt> </dl>

 

