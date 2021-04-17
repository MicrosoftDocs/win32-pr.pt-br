---
title: Comportamentos de teste de colisão de toque
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como as mensagens de teste de toque são processadas pelo Windows que são registradas por meio da função RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766572"
---
# <a name="touch-hit-testing-behaviors"></a>Comportamentos de teste de colisão de toque

As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como as mensagens de teste de toque são processadas pelo Windows que são registradas por meio da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

| Constante/valor | Descrição |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens não são enviadas para a janela de destino, mas são enviadas para janelas filhas.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens são enviadas para a janela de destino.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens não são enviadas para a janela de destino ou janelas filhas.<br/>              |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>WinUser. h |

## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
