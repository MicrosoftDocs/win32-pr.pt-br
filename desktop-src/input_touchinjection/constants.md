---
title: Constantes de injeção de toque
description: Esta seção fornece as especificações de referência para constantes de injeção de toque.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451736"
---
# <a name="touch-injection-constants"></a>Constantes de injeção de toque

Esta seção fornece as especificações de referência para constantes de [injeção de toque](touch-injection-portal.md) .

| Constante/valor | Descrição |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Especifica o número máximo de contatos simultâneos.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Especifica as visualizações de toque padrão.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | Especifica as visualizações de toque indireto.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | Especifica nenhuma visualização de toque.<br/>                     |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 \[ somente aplicativos da área de trabalho\]                                           |
| Servidor mínimo com suporte | Windows Server 2012 \[ somente aplicativos da área de trabalho\]                                 |
| parâmetro                   | WinUser. h |

## <a name="see-also"></a>Confira também

[Referência de injeção de toque](touch-injection-reference.md)
