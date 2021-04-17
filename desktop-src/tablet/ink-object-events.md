---
description: 'A tabela a seguir descreve os threads nos quais os eventos do objeto de tinta podem ser acionados. EventThreadsInkAddedFires no thread de tinta ou no thread do chamador. Um evento InkAdded gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture, é acionado no thread de tinta. InkDeletedFires no thread de tinta ou no thread do chamador. Um evento InkDeleted gerado pela interação do usuário com o objeto InkCollector, o objeto InkOverlay ou o controle InkPicture, é acionado no thread de tinta. '
ms.assetid: 410f7126-5c4c-4c0c-8aa6-c94f15c903fc
title: Eventos de objeto de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0375606b4f4a2f257aa00c360c764972f28c467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461078"
---
# <a name="ink-object-events"></a>Eventos de objeto de tinta

A tabela a seguir descreve os threads nos quais os eventos do objeto de [**tinta**](inkdisp-class.md) podem ser acionados.



| Evento                                    | Threads                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Dispara no thread de tinta ou no thread do chamador.<br/> Um evento [**InkAdded**](inkdisp-inkadded.md) gerado pela interação do usuário com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) , é acionado no thread de tinta.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Dispara no thread de tinta ou no thread do chamador.<br/> Um evento [**InkDeleted**](inkdisp-inkdeleted.md) gerado pela interação do usuário com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) , é acionado no thread de tinta.<br/> |



 

 

 




