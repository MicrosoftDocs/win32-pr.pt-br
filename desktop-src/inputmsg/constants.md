---
title: Constantes de mensagens e notificações de entrada de ponteiro
description: Os tópicos nesta seção fornecem as especificações de referência para as mensagens de entrada do ponteiro e as constantes de notificações.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 600ae37234c64ab313d38666b83f926795b08e21d91f23eeaec68aa68b24b9db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829766"
---
# <a name="pointer-input-messages-and-notifications-constants"></a>Constantes de mensagens e notificações de entrada de ponteiro

Os tópicos nesta seção fornecem as especificações de referência para [as mensagens de entrada do ponteiro e as](messages-and-notifications-portal.md) constantes de notificações.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                             | Descrição                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Estado de chave do modificador**](modifier-key-states-constants.md)<br/>            | Indica quais teclas modificadoras de teclado foram pressionadas na hora em que a entrada estava sendo gerada.<br/>                                                                                                       |
| [**Sinalizadores de caneta**](pen-flags-constants.md)<br/>                               | Os valores que podem aparecer no campo **penFlags** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                         |
| [**Máscara de caneta**](pen-mask-constants.md)<br/>                                 | Os valores que podem aparecer no campo **penMask** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                          |
| [**Alteração do dispositivo do ponteiro**](pointer-device-change-constants.md)<br/>       | Valores que podem ser passados no parâmetro *wParam* da mensagem de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .<br/>                                                                    |
| [**Sinalizadores de ponteiro**](pointer-flags-contants.md)<br/>                        | Os valores que podem aparecer no campo **pointerFlags** da estrutura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                              |
| [**Sinalizadores de mensagem do ponteiro**](pointer-message-flags.md)<br/>                 | Valores que são usados em várias macros de ponteiro (consulte [as macros](macros.md)).<br/>                                                                                                                       |
| [**Sinalizadores de toque**](touch-flags-constants.md)<br/>                           | Os valores que podem aparecer no campo **touchFlags** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                   |
| [**Janela teste de colisão de toque**](touch-hit-testing-window-constants.md)<br/> | Indica como as mensagens para teste de clique de toque são processadas pelo Windows que são registradas por meio da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .<br/> |
| [**Máscara de toque**](touch-mask-constants.md)<br/>                             | Os valores que podem aparecer no campo **touchMask** da estrutura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de mensagem de entrada do ponteiro](wmpointer-reference.md)
</dt> </dl>

 

