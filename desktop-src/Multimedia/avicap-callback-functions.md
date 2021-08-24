---
title: Funções de retorno de chamada AVICap
description: Funções de retorno de chamada AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Classe AVICap, funções de retorno de chamada
- Funções de retorno de chamada do AVICap, sobre
- WM_CAP_SET_CALLBACK_CAPCONTROL mensagem
- WM_CAP_SET_CALLBACK_ERROR mensagem
- WM_CAP_SET_CALLBACK_FRAME mensagem
- WM_CAP_SET_CALLBACK_STATUS mensagem
- WM_CAP_SET_CALLBACK_VIDEOSTREAM mensagem
- WM_CAP_SET_CALLBACK_WAVESTREAM mensagem
- WM_CAP_SET_CALLBACK_YIELD mensagem
- macro capSetCallbackOnCapControl
- capSetCallbackOnErrormacro
- macro capSetCallbackOnFrame
- macro capSetCallbackOnStatus
- macro capSetCallbackOnVideoStream
- macro capSetCallbackOnWaveStream
- macro capSetCallbackOnYield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee000f03df5bb23ed46f3692ded692630c85a292dfe3dccfcd24a8867849d5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691956"
---
# <a name="avicap-callback-functions"></a>Funções de retorno de chamada AVICap

Seu aplicativo pode registrar funções de retorno de chamada com uma janela de captura para que ela Notifique seu aplicativo quando o status for alterado, quando ocorrerem erros, quando os buffers de áudio e de quadros de vídeo forem disponibilizados e para gerar durante a captura de streaming. As mensagens a seguir definem a função de retorno de chamada.



| Mensagem                                                                        | Descrição                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Cap \_ set \_ callback \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Especifica a função de retorno de chamada no aplicativo chamado para fornecer controle preciso sobre o início e o término da captura. Você também pode usar a macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) para enviar esta mensagem.                   |
| [**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-error.md)             | Especifica a função de retorno de chamada no aplicativo chamado quando ocorre um erro. Você também pode usar a macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) para enviar esta mensagem.                                                           |
| [**\_quadro de \_ retorno de \_ chamada Set \_ Cap do WM**](wm-cap-set-callback-frame.md)             | Especifica a função de retorno de chamada no aplicativo chamado quando os quadros de visualização são capturados. Você também pode usar a macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) para enviar esta mensagem.                                               |
| [**WM \_ Cap \_ definir \_ status de retorno de chamada \_**](wm-cap-set-callback-status.md)           | Especifica a função de retorno de chamada no aplicativo chamado quando o status é alterado. Você também pode usar a macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) para enviar esta mensagem.                                                      |
| [**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md) | Especifica a função de retorno de chamada no aplicativo chamado durante a captura de streaming quando um novo buffer de vídeo fica disponível. Você também pode usar a macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) para enviar esta mensagem. |
| [**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-wavestream.md)   | Especifica a função de retorno de chamada no aplicativo chamado durante a captura de streaming quando um novo buffer de áudio fica disponível. Você também pode usar a macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) para enviar esta mensagem.   |
| [**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**](wm-cap-set-callback-yield.md)             | Especifica a função de retorno de chamada no aplicativo chamado ao produzir durante a captura de streaming. Você também pode usar a macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) para enviar esta mensagem.                                         |



 

Os tópicos a seguir descrevem as diferentes funções de retorno de chamada, as notificações enviadas para as funções e seus usos.

 

 




