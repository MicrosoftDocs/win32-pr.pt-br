---
title: PBM_SETRANGE mensagem (Commctrl.h)
description: Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE controles Windows mensagem
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dca4e4be30b50627d8583a67801dc5cb246ef65e9cd267e6d7b3ee3ed7869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170193"
---
# <a name="pbm_setrange-message"></a>Mensagem PBM \_ SETRANGE

Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor de intervalo mínimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor de intervalo máximo. O valor do intervalo mínimo não deve ser negativo. Por padrão, o valor mínimo é zero. O valor de intervalo máximo deve ser maior que o valor de intervalo mínimo. Por padrão, o valor máximo do intervalo é 100.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará os valores de intervalo anteriores se for bem-sucedido ou zero caso contrário. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo anterior e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo anterior.

## <a name="remarks"></a>Comentários

Se você não definir os valores de intervalo, o sistema definirá o valor mínimo como 0 e o valor máximo como 100. Como essa mensagem expressa o intervalo como um inteiro sem sinal de 16 bits, ela pode se estender de 0 a 65.535. O valor mínimo no intervalo pode ser de 0 a 65.535. Da mesma forma, o valor máximo pode ser de 0 a 65.535.

Para definir um intervalo maior, chame [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**PBM \_ GETRANGE**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 

