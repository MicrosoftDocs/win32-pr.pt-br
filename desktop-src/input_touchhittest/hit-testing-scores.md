---
title: Pontuações de teste de toque de toque
description: As constantes a seguir identificam as pontuações de teste de acerto possíveis para um objeto, em relação a outros objetos que intersectam a área de contato de toque.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 18b321272637f4e6931bdc9115e64f8b0553e90e94d8013147ca7a577bad1eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758008"
---
# <a name="touch-hit-testing-scores"></a>Pontuações de teste de toque de toque

As constantes a seguir identificam as pontuações de teste de acerto possíveis para um objeto, em relação a outros objetos que intersectam a área de contato de toque.

| Constante/valor | Descrição |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | O objeto é o destino mais provável.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | O objeto é o destino menos provável.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Cabeçalho<br/>                   | Winuser.h |
