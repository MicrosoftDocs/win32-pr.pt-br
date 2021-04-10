---
title: Método Enumerator. ReadItem (WSManDisp. h)
description: Recupera um item do recurso e retorna uma representação XML do item.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método ReadItem
- Método ReadItem Gerenciamento Remoto do Windows, objeto Enumerator
- Objeto Enumerator Gerenciamento Remoto do Windows, método ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009140"
---
# <a name="enumeratorreaditem-method"></a>Método Enumerator. ReadItem

Recupera um item do recurso e retorna uma representação XML do item.

## <a name="syntax"></a>Sintaxe


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Kit* 
</dt> <dd>

O URI do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A representação XML do item.

## <a name="remarks"></a>Comentários

Para limitar o número de itens lidos, defina a propriedade [**Session.BatchItems**](session-batchitems.md) .

Observe que a liberação do objeto de enumeração limpa todas as solicitações de enumeração pendentes.

O método [**Session. Enumerate**](session-enumerate.md) não obtém uma coleção da mesma maneira que uma [consulta WMI](/windows/desktop/WmiSdk/querying-wmi), como `SELECT * from Win32_LogicalDisk` , retorna uma coleção em um [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset). Para ler um arquivo como um fluxo de texto, crie o objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script e chame o método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para ler cada linha do arquivo. De forma semelhante, você chama o método **Session. enumerar** para obter um objeto [**Enumerator**](enumerator.md) e, em seguida, chamar o método **Enumerator. ReadItem** . Como na leitura do arquivo de texto, você pode verificar a propriedade [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) para verificar se você atingiu o final dos itens de dados.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir chama o método [**Session. enumerar**](session-enumerate.md) para obter uma lista de trabalhos agendados. A sub-rotina DisplayOutput usa o arquivo de transformação XML da ferramenta de linha de comando do WinRM (WsmTxt. Xsl) para gerar os dados em um formato de tabela.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Enumerador**](enumerator.md)
</dt> <dt>

[Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

