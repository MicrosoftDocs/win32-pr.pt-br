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
# <a name="sessiontimeout-property"></a>Propriedade Session. Timeout

Define e obtém a quantidade máxima de tempo, em milissegundos, que o aplicativo cliente aguarda Gerenciamento Remoto do Windows concluir suas operações.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Valor da propriedade

Valor de tempo limite, em milissegundos. Quando o valor de tempo limite for excedido, ocorrerá um erro em tempo de execução.

## <a name="remarks"></a>Comentários

O valor de tempo limite pode ser definido antes de cada operação executada pelo agente. Se um valor de tempo limite não for especificado, o agente definirá o valor de tempo limite.

Durante uma operação de enumeração, o valor de tempo limite não pode ser redefinido enquanto o recurso está sendo enumerado.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir inicia um processo de Calc.exe usando o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) da classe de [**\_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) . O parâmetro *strInputParameters* contém os parâmetros de entrada no formato XML. O script especifica um tempo limite para a sessão.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session.md)
</dt> </dl>

 

