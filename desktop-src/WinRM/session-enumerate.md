---
title: Método Session.Enumerate (WSManDisp.h)
description: Enumera uma tabela, coleta de dados ou recurso de log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerar o método Windows Gerenciamento Remoto
- Enumerar o método Windows Gerenciamento Remoto, Objeto de sessão
- Objeto de sessão Windows Gerenciamento Remoto , Enumerar método
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
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642626"
---
# <a name="sessionenumerate-method"></a>Método Session.Enumerate

Enumera uma tabela, coleta de dados ou recurso de log. Para criar uma consulta, inclua um parâmetro *de filtro* e um parâmetro *de dialeto* em uma enumeração. Você também pode usar um [**objeto ResourceLocator**](resourcelocator.md) para criar consultas. Para obter mais informações, [consulte Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md).

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

*resourceUri* \[ Em\]
</dt> <dd>

O identificador do recurso a ser recuperado.

Esse parâmetro pode conter um dos seguintes:

-   O URI do recurso.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Um [**objeto ResourceLocator.**](resourcelocator.md)
-   Uma referência de ponto de extremidade de endereçamento [*WS,*](windows-remote-management-glossary.md) conforme descrito no padrão WS-Management protocolo. Para obter mais informações sobre a especificação pública [do protocolo WS-Management](ws-management-protocol.md), consulte Página índice [de especificações de gerenciamento](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*filtro* \[ in, opcional\]
</dt> <dd>

Um filtro que define quais itens no recurso são retornados pela enumeração . Quando o recurso é enumerado, somente os itens que corresponderem aos critérios de filtro são retornados. Incluir um *parâmetro* de filtro e *um parâmetro de* dialeto em uma enumeração converte a enumeração em uma consulta. Para ver um exemplo, [consulte Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md).

Se você tiver um [**objeto ResourceLocator**](resourcelocator.md) para o *parâmetro resourceURI,* esse parâmetro não deverá ser usado.

</dd> <dt>

*dialeto* \[ in, opcional\]
</dt> <dd>

O idioma usado pelo filtro. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), um subconjunto de SQL usado pelo WMI, é o único idioma com suporte.

Se você tiver um [**objeto ResourceLocator**](resourcelocator.md) para o *parâmetro resourceURI,* esse parâmetro não deverá ser usado.

</dd> <dt>

*sinalizadores* \[ in, opcional\]
</dt> <dd>

Um parâmetro que deve conter um sinalizador na **\_ \_ enumeração WSManEnumFlags.** Para obter mais informações, consulte [Constantes de enumeração](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um [**objeto Enumerador**](enumerator.md) que contém os resultados da enumeração .

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como limitar chamadas de rede durante uma enumeração, consulte a [**propriedade BatchItems.**](session-batchitems.md)

Esteja ciente de que se os sinalizadores incluirem as [**Constantes**](enumeration-constants.md) de Enumeração **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow,** o serviço de Gerenciamento Remoto do Windows retornará o código de erro **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

Se um filtro for especificado, ele deverá ser um documento válido em relação ao esquema do recurso. O parâmetro de dialeto é opcional. No entanto, se a cadeia de caracteres de filtro começar com <, mas não for um fragmento XML, inclua o parâmetro *de* dialeto ou defina o sinalizador **WSManFlagNonXmlText** no parâmetro *flags.* Para obter mais informações, consulte [**Constantes de enumeração**](enumeration-constants.md).

O método C++ correspondente [**é IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir enumera as instâncias [**\_ logicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em um computador remoto especificado pelo nome de domínio totalmente qualificado (servername.domain.com). Esteja ciente de que liberar o objeto de enumeração limpa as solicitações de enumeração pendentes. A sub-rotina DisplayOutput usa o arquivo de transformação XML da ferramenta de linha de comando Winrm (WsmTxt.xsl) para exibir os dados em um formato tabular.


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
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sessão**](session.md)
</dt> <dt>

[Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

