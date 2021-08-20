---
description: A tabela a seguir descreve em quais threads os eventos da coleção Strokes podem ser ativas. EventThreadsStrkesAddedFires no thread de tinta ou no thread do chamador. Um evento StrokesAdded gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture é a incêndio no thread de tinta. StrokesRemovedFires no thread de tinta ou no thread do chamador. Um evento StrokesRemoved gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture é a incêndio no thread de tinta.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventos da coleção Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589776"
---
# <a name="strokes-collection-events"></a>Eventos da coleção Strokes

A tabela a seguir descreve em quais threads os eventos da coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) podem ser ativas.



| Evento                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Dispara no thread de tinta ou no thread do chamador.<br/> Um [**evento StrokesAdded**](inkstrokes-strokesadded.md) gerado pela interação do usuário com o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture](inkpicture-control-reference.md) é a incêndio no thread de tinta.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Dispara no thread de tinta ou no thread do chamador.<br/> Um [**evento StrokesRemoved**](inkstrokes-strokesremoved.md) gerado pela interação do usuário com o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture](inkpicture-control-reference.md) é a incêndio no thread de tinta.<br/> |



 

 

 
