---
title: Objeto Enumerator (WSManDisp. h)
description: Representa um fluxo de resultados retornados de operações, como uma operação de pull.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- objeto de enumerador Gerenciamento Remoto do Windows
- objeto Enumerator Gerenciamento Remoto do Windows, descrito
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
ms.openlocfilehash: 83799c4c67ad0b0f7c1ad89c77c3abab5989f1231508757c47dfe4c1705d7e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051824"
---
# <a name="enumerator-object"></a>Objeto Enumerator

Representa um fluxo de resultados retornados de operações, como uma operação de pull. Por exemplo, o método [**Session. enumerar**](session-enumerate.md) retorna vários resultados.

## <a name="members"></a>Membros

O objeto **Enumerator** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Enumerator** tem esses métodos.



| Método                                  | Descrição                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Recupera um item do recurso e retorna uma representação XML do item.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **Enumerator** tem essas propriedades.



| Propriedade                                                     | Descrição                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Obtém um valor booliano que indica se há mais itens na coleção.<br/> |
| [**Erro**](enumerator-error.md)<br/>                 | Obtém uma representação XML de informações de erro adicionais.<br/>                         |



 

## <a name="remarks"></a>Comentários

Para iniciar uma enumeração, use [**Session. Enumerate**](session-enumerate.md). Para fazer uma operação [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) que continua lendo itens na enumeração, use [**Enumerator. ReadItem**](enumerator-readitem.md).

O objeto **enumerador** corresponde à interface [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir enumera todos os discos em um computador remoto especificado pelo nome de domínio totalmente qualificado (servername.domain.com). A sub-rotina DisplayOutput formata a saída de dados da mesma maneira que a ferramenta WinRM. cmd.


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

[API de script do WinRM](winrm-scripting-api.md)
</dt> <dt>

[Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





