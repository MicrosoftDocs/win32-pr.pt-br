---
title: Captura de quadro manual
description: Captura de quadro manual
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN mensagem
- WM_CAP_SINGLE_FRAME mensagem
- WM_CAP_SINGLE_FRAME_CLOSE mensagem
- macro capCaptureSingleFrameOpen
- macro capCaptureSingleFrame
- macro capCaptureSingleFrameClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822493"
---
# <a name="manual-frame-capture"></a>Captura de quadro manual

Se você quiser especificar individualmente os quadros a serem capturados em um fluxo de vídeo, poderá controlar a sequência usando o quadro de visualização do [**WM, \_ \_ \_ \_ abrir**](wm-cap-single-frame-open.md)a extremidade do quadro [**\_ \_ único \_**](wm-cap-single-frame.md)e mensagens de [**\_ \_ \_ \_ fechamento do quadro do WM Cap**](wm-cap-single-frame-close.md) (ou as macros [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)e [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ). Normalmente, essas mensagens são usadas para criar animações acrescentando quadros individuais ao arquivo de captura. \_O WM \_ Cap \_ \_ com um único quadro aberto abre um arquivo para uma operação de captura controlada manualmente. \_O quadro do WM Cap \_ \_ captura um quadro individual e o anexa ao arquivo de captura. \_ \_ \_ \_ O fechamento do quadro do WM Cap fecha o arquivo usado para captura manual de quadros.

> [!Note]  
> Este método de captura não dá suporte à captura de áudio simultânea com captura de vídeo.

 

 

 




