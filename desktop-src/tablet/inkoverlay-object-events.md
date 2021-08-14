---
description: 'A tabela a seguir descreve em quais threads os eventos de objeto InkOverlay podem disparar. EventThreadsCursorButtonDownFires no thread de tintaCursorButtonUpFires no thread de tintaCursorDownFires no thread de tintaCursorInRangeFires no thread de tintaCursorOutOfRangeFires no thread de tintaDoubleClick (somente automação). Dispara no thread da interface do usuário do aplicativoDoubleClick (somente Biblioteca Gerenciada). Aplicação no thread de interface do usuário do aplicativoGestureFires no thread de tintaMouseDownFires no thread de interface do usuário do aplicativoMouseMoveFires no thread de interface do usuário do aplicativoMouseUpFires no thread de interface do usuário do aplicativoMouseWheelFires no thread de interface do usuário do aplicativoNewInAirPacketsFires no thread de tintaNewPacketsFires no thread de tintaPfireFires no thread de interface do usuário do aplicativoPaintingFires no thread de interface do usuário do aplicativoSelectionChangedFires no thread de tinta, ou no thread que atualiza o do objeto InkOverlay  Propriedade de seleçãoSelectionChangingFires no thread de tintaSelectionMovedFires no thread de tintaSelectionMovingFires no thread de tintaSelectionResizedFires no thread de tintaSelectionResizingFires no thread de tintaAlterkeFire s no thread de tintaStrstrõesDeletedFires no thread de tintaStreirakesDeletingFires no thread de tintaSystemGestureFires no thread de tintaTabletAddedFires no thread de tintaTabletRemovedFires no thread de tinta '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventos de objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ee197a14edf3ce0aa8595bdbcdb3ea2937d9cf863dcc6e95690088ed8ee96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218959"
---
# <a name="inkoverlay-object-events"></a>Eventos de objeto InkOverlay

A tabela a seguir descreve em quais threads os [**eventos de objeto InkOverlay**](inkoverlay-class.md) podem disparar.



| Evento                                                                             | Threads                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (somente Automação).                  | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (somente Biblioteca Gerenciada). | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Gesto**](inkoverlay-gesture.md)                                             | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Mousedown**](inkoverlay-mousedown.md)                                         | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Mousemove**](inkoverlay-mousemove.md)                                         | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Mouseup**](inkoverlay-mouseup.md)                                             | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Mousewheel**](inkoverlay-mousewheel.md)                                       | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                                             | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Pintura**](inkoverlay-painting.md)                                           | Ativas no thread de interface do usuário do aplicativo<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Ativas no thread de tinta ou no thread que atualiza [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) a propriedade Selection do objeto [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**Selectionchanging**](inkoverlay-selectionchanging.md)                         | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Selectionmoving**](inkoverlay-selectionmoving.md)                             | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Selectionresizing**](inkoverlay-selectionresizing.md)                         | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Curso**](inkoverlay-stroke.md)                                               | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**Systemgesture**](inkoverlay-systemgesture.md)                                 | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Ativas no thread de tinta<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Ativas no thread de tinta<br/>                                                                                                                                        |



 

 

