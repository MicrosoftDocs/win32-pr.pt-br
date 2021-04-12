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
# <a name="sessionput-method"></a>Método Session. put

Atualiza um recurso.

## <a name="syntax"></a>Sintaxe


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

O identificador do recurso a ser atualizado.

Esse parâmetro pode conter um dos elementos contidos na lista a seguir:

-   URI com ou sem [*seletores*](windows-remote-management-glossary.md). Ao chamar o método **Put** para obter um recurso WMI, use a propriedade de chave ou as propriedades do objeto. Por exemplo, no exemplo de código a seguir Visual Basic Scripting Edition (VBScript), a chave é especificada por `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).
-   Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão [protocolo WS-Management](ws-management-protocol.md) . Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*recurso* \[ do no\]
</dt> <dd>

O conteúdo do recurso atualizado.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Reservado. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O XML que contém o conteúdo do recurso atualizado.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir grava dados no objeto [**\_ WMISetting do Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) . Você deve incluir todas as propriedades que não sejam da matriz do objeto no XML do parâmetro de *recurso* . A ordem das propriedades não é significativa.


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

 

