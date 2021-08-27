---
title: Método Session. Create (WSManDisp. h)
description: Cria uma nova instância de um recurso e retorna a referência do ponto de extremidade (EPR) do novo objeto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- criar Gerenciamento Remoto do Windows do método
- criar Gerenciamento Remoto do Windows do método, objeto Session
- objeto de sessão Gerenciamento Remoto do Windows, criar método
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823258"
---
# <a name="sessioncreate-method"></a>Método Session. Create

Cria uma nova instância de um recurso e retorna a [*referência do ponto de extremidade (EPR)*](windows-remote-management-glossary.md) do novo objeto.

## <a name="syntax"></a>Sintaxe


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

Identificador do recurso a ser criado.

Esse parâmetro pode conter um dos seguintes:

-   URI com um ou mais [*seletores*](windows-remote-management-glossary.md). Lembre-se de que o [*plug-in WMI*](windows-remote-management-glossary.md) não dá suporte à criação de qualquer recurso que não seja um ouvinte de [protocolo WS-Management](ws-management-protocol.md) .
-   Objeto [**ResourceLocator**](resourcelocator.md) que pode conter seletores, [*fragmentos*](windows-remote-management-glossary.md)ou [*Opções*](windows-remote-management-glossary.md).
-   Referência de ponto de extremidade [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management. Para obter mais informações sobre a especificação pública para WS-Management protocolo, consulte [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*recurso* 
</dt> <dd>

O XML que contém o conteúdo do recurso.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Reservado. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O EPR do novo recurso.

## <a name="remarks"></a>Comentários

**Session. Create** é usado somente para criar novas instâncias de um recurso. Use o método [**Session. put**](session-put.md) para atualizar as instâncias existentes de um recurso. Depois de obter o novo URI de recurso, você pode chamar [**Session. Get**](session-get.md) para recuperar o novo objeto. O novo objeto contém todas as propriedades que o provedor de recursos atribui ao criar o novo objeto. Por exemplo, se você criar um novo [*ouvinte*](windows-remote-management-glossary.md) de protocolo WS-Management e recuperar o objeto de ouvinte usando **Session. Get**, também obterá as propriedades **Port**, **Enabled** e **listening** .

Lembre-se de que o [*plug-in WMI*](windows-remote-management-glossary.md) não dá suporte à criação de qualquer recurso que não seja um ouvinte de protocolo WS-Management.

A sintaxe a seguir é usada para chamar esse método.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir chama **Session. Create** para criar um ouvinte no computador local.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

