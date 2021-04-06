---
title: Métodos opcionais em interfaces de controle
description: Métodos opcionais em interfaces de controle
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1409b1c8d22f85a48829c07155e03379fc79103c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916052"
---
# <a name="optional-methods-in-control-interfaces"></a>Métodos opcionais em interfaces de controle

A implementação de uma interface não significa necessariamente que a implementação de todos os métodos dessa interface faça mais nada do que retornar E \_ NOTIMPL ou S \_ OK, conforme apropriado. A tabela a seguir identifica os métodos das interfaces listadas no tópico [o que dá suporte a uma interface significa](what-support-for-an-interface-means.md) que um controle pode implementar dessa maneira. Qualquer método não listado aqui deverá ser totalmente implementado se a interface tiver suporte.



| IOleControl                                                                                                   | Comentários                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **onmnemônico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obrigatório para controles com mnemônicos.<br/>                              |
| [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obrigatório para controles que usam Propriedades de ambiente.<br/>                 |
| [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Ver [evento congelando](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obrigatório se o controle não estiver marcado com OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obrigatório se o controle não estiver marcado com OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Opcional<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Opcional<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obrigatório somente para \_ conteúdo DVASPECT<br/>                                |
| [**Getextensão**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obrigatório somente para \_ conteúdo DVASPECT<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Opcional<br/>                                                            |
| [**Doverbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Veja a observação 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcional<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Opcional<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcional<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Congelamento**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Opcional<br/>                                                            |
| [**Descongelar**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Opcional<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Opcional<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Confira a observação 2<br/>                                                          |



 

1.  Um controle com páginas de propriedades deve dar suporte a [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) para as \_ Propriedades OLEIVERB e os \_ verbos primários OLEIVERB. Um controle que pode ser ativo deve oferecer suporte ao **doverbs** para o \_ verbo OLEIVERB INPLACEACTIVATE. Um controle que pode ser de interface do usuário ativa também deve oferecer suporte a **doverbs** para o \_ verbo OLEIVERB UIACTIVATE.
2.  Se um controle oferecer suporte a [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) e puder retornar um valor preciso, ele deverá fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





