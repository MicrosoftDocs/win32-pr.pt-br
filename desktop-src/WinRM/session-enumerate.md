---
title: Método Session. Enumeration (WSManDisp. h)
description: Enumera uma tabela, uma coleção de dados ou um recurso de log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Enumerate
- Método Enumerate Gerenciamento Remoto do Windows, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, método Enumerate
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009139"
---
# <a name="sessionenumerate-method"></a>Método Session. Enumeration

Enumera uma tabela, uma coleção de dados ou um recurso de log. Para criar uma consulta, inclua um parâmetro de *filtro* e um parâmetro de *dialeto* em uma enumeração. Você também pode usar um objeto [**ResourceLocator**](resourcelocator.md) para criar consultas. Para obter mais informações, consulte [enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="syntax"></a>Sintaxe


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

O identificador do recurso a ser recuperado.

Esse parâmetro pode conter um dos seguintes:

-   O URI do recurso.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Um objeto [**ResourceLocator**](resourcelocator.md) .
-   Uma referência de ponto de extremidade do [*WS-Addressing*](windows-remote-management-glossary.md) , conforme descrito no padrão do protocolo WS-Management. Para obter mais informações sobre a especificação pública para [protocolo WS-Management](ws-management-protocol.md), consulte a [página de índice de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Filtrar* \[ em, opcional\]
</dt> <dd>

Um filtro que define quais itens no recurso são retornados pela enumeração. Quando o recurso é enumerado, somente os itens que correspondem aos critérios de filtro são retornados. A inclusão de um parâmetro de *filtro* e um parâmetro de *dialeto* em uma enumeração converte a enumeração em uma consulta. Para obter um exemplo, consulte [consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md).

Se você tiver um objeto [**ResourceLocator**](resourcelocator.md) para o parâmetro *ResourceURI* , esse parâmetro não deverá ser usado.

</dd> <dt>

*dialeto* \[ em, opcional\]
</dt> <dd>

O idioma usado pelo filtro. O [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), um subconjunto de SQL usado pelo WMI, é o único idioma com suporte.

Se você tiver um objeto [**ResourceLocator**](resourcelocator.md) para o parâmetro *ResourceURI* , esse parâmetro não deverá ser usado.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Um parâmetro que deve conter um sinalizador na enumeração **\_ \_ WSManEnumFlags** . Para obter mais informações, consulte [constantes de enumeração](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto [**enumerador**](enumerator.md) que contém os resultados da enumeração.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como limitar chamadas de rede durante uma enumeração, consulte a propriedade [**BatchItems**](session-batchitems.md) .

Lembre-se de que, se os sinalizadores incluírem as [**constantes de enumeração**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , gerenciamento remoto do Windows serviço retornará o erro de código de erro o **modo de polimorfismo do \_ WSMan \_ \_ \_ sem suporte**.

Se um filtro for especificado, ele deverá ser um documento válido em relação ao esquema do recurso. O parâmetro dialeto é opcional. No entanto, se a cadeia de caracteres de filtro começar com <, mas não for um fragmento XML, inclua o parâmetro *dialeto* ou defina o sinalizador **WSManFlagNonXmlText** no parâmetro *flags* . Para obter mais informações, consulte [**constantes de enumeração**](enumeration-constants.md).

O método C++ correspondente é [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir enumera as instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em um computador remoto especificado pelo servername.domain.com (nome de domínio totalmente qualificado). Lembre-se de que a liberação do objeto de enumeração limpa as solicitações de enumeração pendentes. A sub-rotina DisplayOutput usa o arquivo de transformação XML da ferramenta de linha de comando do WinRM (WsmTxt. Xsl) para gerar os dados em um formato de tabela.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

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
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session.md)
</dt> <dt>

[Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

