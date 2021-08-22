---
title: Método Session. Get (WSManDisp. h)
description: Recupera o recurso especificado pelo URI e retorna uma representação XML da instância atual do recurso.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- método Get Gerenciamento Remoto do Windows
- método Get Gerenciamento Remoto do Windows, objeto Session
- objeto de sessão Gerenciamento Remoto do Windows, método Get
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
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642556"
---
# <a name="sessionget-method"></a>Método Session. Get

Recupera o recurso especificado pelo [*URI*](windows-remote-management-glossary.md) e retorna uma representação XML da instância atual do recurso.

## <a name="syntax"></a>Sintaxe


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

O identificador do recurso a ser recuperado.

Esse parâmetro pode conter um dos seguintes:

-   Um URI com ou sem [*seletores*](windows-remote-management-glossary.md). Ao chamar o método **Get** com um seletor para obter um recurso WMI, use a propriedade de chave ou as propriedades do objeto. por exemplo, no exemplo de código a seguir Visual Basic scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` . Para classes singleton, como [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), você não pode usar um seletor.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Um objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).
-   Uma referência de ponto de extremidade do [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management. Para obter mais informações sobre a especificação pública para [protocolo WS-Management](ws-management-protocol.md), consulte a [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Reservado. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma representação XML do recurso.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir recupera a representação XML da instância do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa o serviço Winmgmt do WMI no computador local.


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



O exemplo de código VBScript a seguir recupera a instância de serviço do WMI Winmgmt de um computador remoto. O computador remoto é identificado pelo nome de domínio totalmente qualificado (servername.domain.com). A única diferença entre a versão local e a remota é a especificação do computador remoto na chamada para [**WSMan. CreateSession**](wsman-createsession.md).


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

 

