---
description: 'A tabela a seguir descreve em quais threads os eventos de objeto InkOverlay podem ser acionados. EventThreadsCursorButtonDownFires na threadCursorButtonUpFires de tinta na Ink threadCursorDownFires no threadCursorInRangeFires de tinta no threadCursorOutOfRangeFires de tinta na tinta threadDoubleClick (somente automação). Acionado na interface do usuário (IU) do aplicativo threadDoubleClick (somente biblioteca gerenciada). Acionado na interface do usuário do aplicativo threadGestureFires no threadMouseDownFires de tinta na interface do usuário do aplicativo threadMouseMoveFires na interface do usuário do aplicativo threadMouseUpFires no threadMouseWheelFires da interface do usuário do aplicativo na interface do usuário do aplicativo threadNewInAirPacketsFires no thread de tinta do threadNewPacketsFires na barra de entrada threadPaintedFires no threadPaintingFires da interface do usuário do aplicativo na threadSelectionChangedFires de IU do aplicativo, ou no thread que atualiza a seleção do objeto InkOverlay propertySelectionChangingFires no threadSelectionMovedFires de tinta na tinta threadSelectionMovingFires no threadSelectionResizedFires de tinta na tinta threadSelectionResizingFires on o threadStrokeFires de tinta na threadStrokesDeletedFires de tinta na tinta threadStrokesDeletingFires no threadSystemGestureFires de tinta no threadTabletAddedFires de tinta do threadTabletRemovedFires de tinta no thread de tinta '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventos de objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764383"
---
# <a name="inkoverlay-object-events"></a>Eventos de objeto InkOverlay

A tabela a seguir descreve em quais threads os eventos de objeto [**InkOverlay**](inkoverlay-class.md) podem ser acionados.



| Evento                                                                             | Threads                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (somente automação).                  | Acionado no thread da interface do usuário (IU) do aplicativo<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (somente biblioteca gerenciada). | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Gesto**](inkoverlay-gesture.md)                                             | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**MouseDown**](inkoverlay-mousedown.md)                                         | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Ocorra**](inkoverlay-mousemove.md)                                         | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**MouseWheel**](inkoverlay-mousewheel.md)                                       | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                                             | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**Pintura**](inkoverlay-painting.md)                                           | Acionado no thread da interface do usuário do aplicativo<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Dispara no thread de tinta ou no thread que atualiza a propriedade de [**seleção**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) do objeto [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**Pincel**](inkoverlay-stroke.md)                                               | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Acionado no thread de tinta<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Acionado no thread de tinta<br/>                                                                                                                                        |



 

 

