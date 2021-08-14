---
title: Classe StreamSelectOperation
description: Registra um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetMuteAsync é concluída e fornece um método que retorna os resultados da operação. | Classe StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API de streaming de mídia de classe StreamSelectOperation
- API de streaming de mídia de classe StreamSelectOperation, descrita
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161434aad9c4eb20960950ba2dd1979c9caaa2ccc5bbe3c2683ee3e4f839a0b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461556"
---
# <a name="streamselectoperation-class"></a>Classe StreamSelectOperation

Registra um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) é concluída e fornece um método que retorna os resultados da operação.

**StreamSelectOperation** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **StreamSelectOperation** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Retorna os resultados da operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).<br/> |



 

### <a name="properties"></a>Propriedades

A classe **StreamSelectOperation** tem essas propriedades.



| Propriedade                                                        | Tipo de acesso           | Descrição                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Concluído**](streamselectoperation-completed.md)<br/> | Leitura/gravação<br/> | Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) é concluída.<br/> |



 

 

