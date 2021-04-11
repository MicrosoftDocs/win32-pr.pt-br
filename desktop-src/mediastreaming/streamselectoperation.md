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
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172775"
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



 

 

