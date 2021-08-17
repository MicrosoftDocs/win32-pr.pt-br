---
title: Método Session. Invoke (WSManDisp. h)
description: Invoca um método e retorna resultados da chamada de método.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Invoke
- método Invoke Gerenciamento Remoto do Windows, objeto Session
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
ms.openlocfilehash: ac2afa20390890c53a7362d776c1df7c84d0a638e7fcb10269c901d194a50dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743247"
---
# <a name="sessioninvoke-method"></a>Método Session. Invoke

Invoca um método e retorna resultados da chamada de método.

## <a name="syntax"></a>Sintaxe


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*actionUri* \[ no\]
</dt> <dd>

O URI do método a ser invocado.

</dd> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

O identificador do recurso a ser recuperado.

Esse parâmetro pode conter um dos seguintes:

-   URI com ou sem [*seletores*](windows-remote-management-glossary.md). no exemplo a seguir Visual Basic scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).
-   Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão [protocolo WS-Management](ws-management-protocol.md) . Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*parâmetros* \[ do no\]
</dt> <dd>

A representação XML da entrada para o método. Essa cadeia de caracteres deve ser fornecida, ou esse método falhará.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Reservado. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A representação XML da saída do método.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir inicia um processo de Calc.exe. O parâmetro *strInputParameters* contém os parâmetros de entrada no formato XML. O único parâmetro de entrada necessário para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe [**de \_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) é a linha de comando a ser executada.


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



O exemplo de código VBScript a seguir chama o método **Session. Invoke** para executar o método [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service). O método **StopService** não tem parâmetros de entrada. No entanto, o método **Invoke** requer uma cadeia de caracteres XML no parâmetro *Parameters* .


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sessão**](session.md)
</dt> </dl>

 

