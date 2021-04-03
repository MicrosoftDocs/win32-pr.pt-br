---
title: Métodos opcionais
description: Métodos opcionais
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084914"
---
# <a name="optional-methods"></a>Métodos opcionais

Um componente OLE pode implementar uma interface sem implementar toda a semântica de cada método na interface, em vez de retornar E \_ NOTIMPL ou S \_ OK conforme apropriado. A tabela a seguir descreve os métodos que um contêiner de controle ActiveX não precisa implementar (ou seja, o contêiner de controle pode retornar E \_ NOTIMPL).

A tabela a seguir descreve os métodos opcionais; Observe que o método ainda deve existir, mas pode simplesmente retornar E \_ NOTIMPL em vez de implementar a semântica real. Observe que qualquer método de uma interface obrigatória que não esteja listada abaixo deve ser considerado obrigatório e não pode retornar e \_ NOTIMPL.

## <a name="ioleclientsite"></a>IOleClientSite



| Método                                                     | Comentários                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Salvar como**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necessário para que a persistência seja suportada com êxito.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Necessário somente se o contêiner der suporte à vinculação de controles em seu próprio formulário ou documento.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Método                                                                     | Comentários                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Opcional<br/>                                      |
| [**Rolagem**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Pode retornar S \_ false sem ação.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Pode retornar S \_ OK sem ação.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | A desativação é obrigatória; Desfazer é opcional. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Método                                                                          | Comentários                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necessário para contêineres que dão suporte a controles estendidos.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necessário para contêineres que desejam incluir suas próprias páginas de propriedades para manipular propriedades de controle estendido além daqueles fornecidos por um controle.<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Pode retornar S \_ false sem ação.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Opcional<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (Propriedades de ambiente)



| Método                      | Comentários                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.<br/> |
| GetTypeInfo<br/>      | Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.<br/> |
| GetIDsOfNames<br/>    | Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (coletor de eventos)



| Método                      | Comentários                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.<br/> |
| GetTypeInfo<br/>      | O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.<br/> |
| GetIDsOfNames<br/>    | O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Método                                                                           | Comentários                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necessário para contêineres com interface do usuário de menu (que é opcional)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necessário para contêineres com interface do usuário de menu (que é opcional)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necessário para contêineres com interface do usuário de menu (que é opcional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Necessário somente para contêineres que têm uma linha de status<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Opcional<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Opcional<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Método                                                                    | Comentários                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Somente se houver suporte para vinculação a controles ou a outras incorporações no contêiner, como isso é necessário para a associação de moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Como para ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Retorna todos os controles ActiveX por meio de um enumerador com [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), mas não necessariamente todos os objetos (porque não há nenhuma garantia de que todos os objetos são controles ActiveX; alguns podem ser controles regulares do Windows).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

