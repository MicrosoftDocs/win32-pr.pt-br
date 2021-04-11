---
title: Método Session. Get (WSManDisp. h)
description: Recupera o recurso especificado pelo URI e retorna uma representação XML da instância atual do recurso.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Método Get Gerenciamento Remoto do Windows
- Método Get Gerenciamento Remoto do Windows, objeto Session
- Objeto de sessão Gerenciamento Remoto do Windows, método Get
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295852"
---
# <a name="sessionget-method"></a><span data-ttu-id="4a46e-106">Método Session. Get</span><span class="sxs-lookup"><span data-stu-id="4a46e-106">Session.Get method</span></span>

<span data-ttu-id="4a46e-107">Recupera o recurso especificado pelo [*URI*](windows-remote-management-glossary.md) e retorna uma representação XML da instância atual do recurso.</span><span class="sxs-lookup"><span data-stu-id="4a46e-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a46e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a46e-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4a46e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a46e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a46e-110">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a46e-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a46e-111">O identificador do recurso a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="4a46e-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="4a46e-112">Esse parâmetro pode conter um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4a46e-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="4a46e-113">Um URI com ou sem [*seletores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4a46e-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="4a46e-114">Ao chamar o método **Get** com um seletor para obter um recurso WMI, use a propriedade de chave ou as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="4a46e-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="4a46e-115">Por exemplo, no exemplo de código a seguir Visual Basic Scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="4a46e-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="4a46e-116">Para classes singleton, como [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), você não pode usar um seletor.</span><span class="sxs-lookup"><span data-stu-id="4a46e-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="4a46e-117">Um objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4a46e-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="4a46e-118">Uma referência de ponto de extremidade do [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="4a46e-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="4a46e-119">Para obter mais informações sobre a especificação pública para [protocolo WS-Management](ws-management-protocol.md), consulte a [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="4a46e-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="4a46e-120">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4a46e-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a46e-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4a46e-121">Reserved.</span></span> <span data-ttu-id="4a46e-122">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="4a46e-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a46e-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a46e-123">Return value</span></span>

<span data-ttu-id="4a46e-124">Uma representação XML do recurso.</span><span class="sxs-lookup"><span data-stu-id="4a46e-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="4a46e-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a46e-125">Examples</span></span>

<span data-ttu-id="4a46e-126">O exemplo de código VBScript a seguir recupera a representação XML da instância do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa o serviço Winmgmt do WMI no computador local.</span><span class="sxs-lookup"><span data-stu-id="4a46e-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



<span data-ttu-id="4a46e-127">O exemplo de código VBScript a seguir recupera a instância de serviço do WMI Winmgmt de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="4a46e-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="4a46e-128">O computador remoto é identificado pelo nome de domínio totalmente qualificado (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="4a46e-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="4a46e-129">A única diferença entre a versão local e a remota é a especificação do computador remoto na chamada para [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="4a46e-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



## <a name="requirements"></a><span data-ttu-id="4a46e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a46e-130">Requirements</span></span>



| <span data-ttu-id="4a46e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a46e-131">Requirement</span></span> | <span data-ttu-id="4a46e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4a46e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a46e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a46e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4a46e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a46e-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4a46e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a46e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4a46e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a46e-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4a46e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a46e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a46e-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a46e-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a46e-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="4a46e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a46e-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a46e-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a46e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a46e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a46e-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a46e-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a46e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4a46e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a46e-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a46e-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a46e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a46e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a46e-146">**Session**</span><span class="sxs-lookup"><span data-stu-id="4a46e-146">**Session**</span></span>](session.md)
</dt> </dl>

 

