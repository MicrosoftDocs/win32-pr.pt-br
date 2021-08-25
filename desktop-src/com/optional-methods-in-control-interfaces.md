---
title: Métodos opcionais em interfaces de controle
description: Métodos opcionais em interfaces de controle
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859286"
---
# <a name="optional-methods-in-control-interfaces"></a>Métodos opcionais em interfaces de controle

Implementar uma interface não significa necessariamente implementar todos os métodos dessa interface para fazer mais do que retornar E NOTIMPL ou \_ S OK conforme \_ apropriado. A tabela a seguir identifica os métodos das interfaces listadas no tópico [What Support for an Interface Means](what-support-for-an-interface-means.md) que um controle pode implementar dessa maneira. Qualquer método não listado aqui deverá ser totalmente implementado se a interface tiver suporte.



| Iolecontrol                                                                                                   | Comentários                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo,**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obrigatório para controles com mnemônicos.<br/>                              |
| [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obrigatório para controles que usam propriedades de ambiente.<br/>                 |
| [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Consulte [Congelamento de eventos](event-freezing.md)<br/>                            |
| Ioleobject                                                                                                    |                                                                                |
| [**Setmoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obrigatório se o controle não estiver marcado com OLEMISC \_ CANTLINKINSIDE<br/> |
| [**Getmoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obrigatório se o controle não estiver marcado com OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Opcional<br/>                                                            |
| [**Getclipboarddata**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Opcional<br/>                                                            |
| [**Setextent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obrigatório somente para DVASPECT \_ CONTENT<br/>                                |
| [**Getextent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obrigatório somente para DVASPECT \_ CONTENT<br/>                                |
| [**Setcolorscheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Opcional<br/>                                                            |
| [**Doverb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Consulte a observação 1<br/>                                                          |
| Ioleinplaceobject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcional<br/>                                                            |
| [**Reactivateandundo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Opcional<br/>                                                            |
| Ioleinplaceactiveobject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcional<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Congelamento**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Opcional<br/>                                                            |
| [**Descongelar**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Opcional<br/>                                                            |
| [**Getcolorset**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Opcional<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**Getsizemax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Confira a observação 2<br/>                                                          |



 

1.  Um controle com páginas de propriedades deve dar suporte a [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) para os verbos OLEIVERB PROPERTIES e \_ OLEIVERB \_ PRIMARY. Um controle que pode ser ativo deve dar suporte a **DoVerb** para o verbo OLEIVERB \_ INPLACEACTIVATE. Um controle que pode ser ativo da interface do usuário também deve dar suporte a **DoVerb** para o verbo OLEIVERB \_ UIACTIVATE.
2.  Se um controle for [**compatível com IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) e puder retornar um valor preciso, ele deverá fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





