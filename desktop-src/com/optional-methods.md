---
title: Métodos opcionais
description: Métodos opcionais
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64f4b22693c77295d3a21cfb59055f9a232d08bb1426d995f710bbf24073d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130038"
---
# <a name="optional-methods"></a>Métodos opcionais

Um componente OLE pode implementar uma interface sem implementar toda a semântica de cada método na interface, em vez disso, retornar E NOTIMPL ou \_ S OK conforme \_ apropriado. A tabela a seguir descreve os métodos que um contêiner de controle ActiveX não é necessário implementar (ou seja, o contêiner de controle pode retornar E \_ NOTIMPL).

A tabela a seguir descreve métodos opcionais; observe que o método ainda deve existir, mas pode simplesmente retornar E NOTIMPL em vez \_ de implementar a semântica real. Observe que qualquer método de uma interface obrigatória que não está listada abaixo deve ser considerado obrigatório e pode não retornar E \_ NOTIMPL.

## <a name="ioleclientsite"></a>Ioleclientsite



| Método                                                     | Comentários                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necessário para que a persistência tenha suporte com êxito.<br/>                                       |
| [**Getmoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Necessário somente se o contêiner dá suporte à vinculação a controles em seu próprio formulário ou documento.<br/> |



 

## <a name="ioleinplacesite"></a>Ioleinplacesite



| Método                                                                     | Comentários                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Opcional<br/>                                      |
| [**Rolar**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Pode retornar S \_ FALSE sem ação.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Pode retornar S \_ OK sem nenhuma ação.<br/>              |
| [**DesativarAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | A desativação é obrigatória; Desfazer é opcional. <br/> |



 

## <a name="iolecontrolsite"></a>Iolecontrolsite



| Método                                                                          | Comentários                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necessário para contêineres que suportam controles estendidos.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necessário para contêineres que desejam incluir suas próprias páginas de propriedades para lidar com propriedades de controle estendidas, além daqueles fornecidos por um controle .<br/> |
| [**Translateaccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Pode retornar S \_ FALSE sem ação.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Opcional<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (propriedades de ambiente)



| Método                      | Comentários                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| Gettypeinfocount<br/> | Necessário para contêineres que suportam propriedades de ambiente não padrão.<br/> |
| GetTypeInfo<br/>      | Necessário para contêineres que suportam propriedades de ambiente não padrão.<br/> |
| Getidsofnames<br/>    | Necessário para contêineres que suportam propriedades de ambiente não padrão.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (sink de evento)



| Método                      | Comentários                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| Gettypeinfocount<br/> | O controle conhece suas próprias informações de tipo, portanto, não precisa chamar isso.<br/> |
| GetTypeInfo<br/>      | O controle conhece suas próprias informações de tipo, portanto, não precisa chamar isso.<br/> |
| Getidsofnames<br/>    | O controle conhece suas próprias informações de tipo, portanto, não precisa chamar isso.<br/> |



 

## <a name="ioleinplaceframe"></a>Ioleinplaceframe



| Método                                                                           | Comentários                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necessário para contêineres com interface do usuário do menu (que é opcional)<br/>    |
| [**Setmenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necessário para contêineres com interface do usuário do menu (que é opcional)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necessário para contêineres com interface do usuário do menu (que é opcional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Necessário somente para contêineres que têm uma linha de status<br/>        |
| [**Enablemodeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Opcional<br/>                                                     |
| [**Translateaccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Opcional<br/>                                                     |



 

## <a name="iolecontainer"></a>Iolecontainer



| Método                                                                    | Comentários                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Parsedisplayname**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Somente se a vinculação a controles ou outras incorporações no contêiner tiver suporte, pois isso é necessário para a associação de moniker.<br/>                                                                                                                  |
| [**Lockcontainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Quanto a ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**Enumobjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Retorna todos os controles ActiveX por meio de um enumerador com [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), mas não necessariamente todos os objetos (porque não há nenhuma garantia de que todos os objetos são controles ActiveX; alguns podem ser controles Windows regulares).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

