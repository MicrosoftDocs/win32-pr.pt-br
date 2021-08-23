---
title: Objeto ResourceLocator (WSManDisp.h)
description: Fornece o caminho para um recurso. Você pode usar um objeto ResourceLocator em vez de um URI de recurso em operações de objeto session, como Session.Get, Session.Put ou Session.Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Objeto ResourceLocator Windows Gerenciamento Remoto
- Objeto ResourceLocator Windows Gerenciamento Remoto , descrito
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d3287c02949326b672f550271ba3472e6cb16abb6748efb4a80de425c40e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642866"
---
# <a name="resourcelocator-object"></a>Objeto ResourceLocator

Um objeto que fornece o caminho para um recurso. Você pode usar um objeto **ResourceLocator** em [](session.md) vez de um [*URI*](windows-remote-management-glossary.md) de recurso em operações de objeto session, como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

Esse objeto permite que você:

-   Adicione um ou mais [*seletores que*](windows-remote-management-glossary.md) identificam uma instância específica de um recurso. Isso é o mesmo que fornecer um valor de chave no URI do recurso para um recurso que usa chaves. Para obter mais informações, [**consulte ResourceLocator.AddSelector**](resourcelocator-addselector.md). Você pode fazer uma operação semelhante usando o *parâmetro filter* em uma chamada para [**Session.Enumerate**](session-enumerate.md).
-   [*Especifique um caminho*](windows-remote-management-glossary.md) de fragmento e um dialeto para obter apenas uma propriedade de um recurso. Você também pode especificar um ou todos os elementos de uma propriedade de matriz fornecendo o índice da matriz. Para obter mais informações, [**consulte ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).
-   Adicione uma ou mais [*opções que*](windows-remote-management-glossary.md) uma fonte de dados pode exigir para processar uma solicitação. Para obter mais informações, [**consulte ResourceLocator.AddOption**](resourcelocator-addoption.md).

Para obter mais informações, [consulte Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Membros

O **objeto ResourceLocator** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto ResourceLocator** tem esses métodos.



| Método                                                   | Descrição                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Adiciona dados adicionais necessários para processar a solicitação.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Adiciona um [*seletor*](windows-remote-management-glossary.md) ao **objeto ResourceLocator.**<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Remove todas as [*opções*](windows-remote-management-glossary.md) do **objeto ResourceLocator.**<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Remove todos os seletores de um **objeto ResourceLocator.**<br/>                                                            |



 

### <a name="properties"></a>Propriedades

O **objeto ResourceLocator** tem essas propriedades.



| Propriedade                                                                          | Tipo de acesso           | Descrição                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | Leitura/gravação<br/> | Obtém ou define o dialeto de idioma de um [*fragmento de*](windows-remote-management-glossary.md) [*recurso.*](windows-remote-management-glossary.md)<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o caminho para um [*fragmento de*](windows-remote-management-glossary.md) [*recurso*](windows-remote-management-glossary.md) ou propriedade.<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Leitura/gravação<br/> | Obtém ou define o **valor MustUnderstandOptions** para o **objeto ResourceLocator.**<br/>                                                                                                         |
| [**Resourceuri**](resourcelocator-resourceuri.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o [*URI do*](windows-remote-management-glossary.md) recurso em **um objeto ResourceLocator.**<br/>                                                          |



 

## <a name="remarks"></a>Comentários

O **objeto ResourceLocator** corresponde à interface **IWSManResourceLocator.**

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir obtém as propriedades **NumberOfLogicalProcessors** e **NumberOfCores** de uma instância específica do [**processador Win32 \_**](/windows/desktop/CIMWin32Prov/win32-processor).


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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

[API de Script WinRM](winrm-scripting-api.md)
</dt> </dl>

 

