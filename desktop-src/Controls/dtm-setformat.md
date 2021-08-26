---
title: DTM_SETFORMAT mensagem (Commctrl.h)
description: Define a exibição de um controle DTP (selador de data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a macro DateTime \_ SetFormat.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT controles Windows mensagem
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d4bb08694b63c21f1790d0a1366dd34d1083592bdeb62d532a32a96be3857a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877856"
---
# <a name="dtm_setformat-message"></a>Mensagem SETFORMAT de DTM \_

Define a exibição de um controle DTP (selador de data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a [**macro DateTime \_ SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres de formato terminada [em](date-and-time-picker-controls.md) zero que define a exibição desejada. Definir esse parâmetro como **NULL** redefini o controle para a cadeia de caracteres de formato padrão para o estilo atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="remarks"></a>Comentários

É aceitável incluir caracteres extras dentro da cadeia de caracteres de formato para produzir uma exibição mais rica. No entanto, quaisquer caracteres não format devem ser incluídos entre aspas simples. Por exemplo, a cadeia de caracteres de formato "'Today is: 'hh':'m':'s ddddMMMdd', 'aaa" produziria uma saída como "Today is: 04:22:31 Tuesday Mar 23, 1996".

> [!Note]  
> Um controle DTP controla as alterações de localidade quando está usando a cadeia de caracteres de formato padrão. Se você definir uma cadeia de caracteres de formato personalizado, ela não será atualizada em resposta a alterações de localidade.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) e **DTM \_ SETFORMATA** (ANSI)<br/>               |



 

 





