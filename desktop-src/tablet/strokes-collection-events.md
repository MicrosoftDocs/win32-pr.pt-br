---
description: A tabela a seguir descreve os threads nos quais os eventos de coleção de traços podem ser acionados. EventThreadsStrokesAddedFires no thread de tinta ou no thread do chamador. Um evento StrokesAdded gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture, é acionado no thread de tinta. StrokesRemovedFires no thread de tinta ou no thread do chamador. Um evento StrokesRemoved gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture, é acionado no thread de tinta.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventos de coleção Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765360"
---
# <a name="strokes-collection-events"></a>Eventos de coleção Strokes

A tabela a seguir descreve os threads nos quais os eventos de coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) podem ser acionados.



| Evento                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Dispara no thread de tinta ou no thread do chamador.<br/> Um evento [**StrokesAdded**](inkstrokes-strokesadded.md) gerado pela interação do usuário com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) , é acionado no thread de tinta.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Dispara no thread de tinta ou no thread do chamador.<br/> Um evento [**StrokesRemoved**](inkstrokes-strokesremoved.md) gerado pela interação do usuário com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) , é acionado no thread de tinta.<br/> |



 

 

 
