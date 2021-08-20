---
title: Caixas de diálogo de vídeo
description: Caixas de diálogo de vídeo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE mensagem
- macro capDlgVideoSource
- WM_CAP_DLG_VIDEOFORMAT mensagem
- macro capDlgVideoFormat
- WM_CAP_DLG_VIDEODISPLAY mensagem
- macro capDlgVideoDisplay
- WM_CAP_DLG_VIDEOCOMPRESSION mensagem
- macro capDlgVideoCompression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93674b8ed4e6f6ff594013cc27825aea601cc005fc082ca8a8954b661c1f4317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135554"
---
# <a name="video-dialog-boxes"></a>Caixas de diálogo de vídeo

Cada driver de captura pode fornecer até quatro caixas de diálogo para controlar aspectos da digitalização de vídeo e do processo de captura e definir atributos de compactação usados para reduzir o tamanho dos dados de vídeo. O conteúdo dessas caixas de diálogo é definido pelo driver de captura de vídeo.

A caixa de diálogo fonte de vídeo controla a seleção de canais de entrada de vídeo e parâmetros que afetam a imagem de vídeo que está sendo digitalizada no buffer de quadros. Essa caixa de diálogo enumera os tipos de sinais que conectam a fonte de vídeo ao cartão de captura (normalmente SVHS e entradas de composição) e fornece controles para alterar o matiz, o contraste ou a saturação. Se a caixa de diálogo for suportada por um driver de captura de vídeo, você poderá exibi-la e atualizá-la usando a mensagem de exibição de [**imagem do WM \_ Cap \_ DLG \_**](wm-cap-dlg-videosource.md) (ou a macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).

A caixa de diálogo formato de vídeo controla a seleção das dimensões de quadros de vídeo digitalizadas e as opções de compactação de imagem e de compressão do vídeo capturado. Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).

A caixa de diálogo exibição de vídeo controla a aparência do vídeo no monitor durante a captura. Os controles nessa caixa de diálogo não têm efeito sobre os dados de vídeo digitalizados, mas podem afetar a apresentação do sinal digitalizado. Por exemplo, os dispositivos de captura que dão suporte à sobreposição podem permitir a alteração de matiz e saturação, a cor da chave ou o alinhamento da sobreposição. Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) (ou a macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).

A caixa de diálogo compactação de vídeo controla os atributos de compactação de vídeo post-Capture. Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) (ou a macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).

 

 




