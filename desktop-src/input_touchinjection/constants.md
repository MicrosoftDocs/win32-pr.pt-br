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
ms.openlocfilehash: 76a763a7153bbb9aa67254ffeb5e994a55426e43
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187735"
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
| Cliente mínimo com suporte | \[Somente aplicativos de área de trabalho do Windows 8\]                                           |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2012\]                                 |
| parâmetro                   | WinUser. h |

## <a name="see-also"></a>Confira também

[Referência de injeção de toque](touch-injection-reference.md)
