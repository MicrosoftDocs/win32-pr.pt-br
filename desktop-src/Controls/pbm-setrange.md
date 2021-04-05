---
title: Mensagem de PBM_SETRANGE (commctrl. h)
description: Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Controles de PBM_SETRANGE de mensagens do Windows
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
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824586"
---
# <a name="pbm_setrange-message"></a>\_Mensagem SETRANGE do PBM

Define os valores mínimo e máximo para uma barra de progresso e redesenha a barra para refletir o novo intervalo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor de intervalo mínimo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor de intervalo máximo. O valor mínimo do intervalo não deve ser negativo. Por padrão, o valor mínimo é zero. O valor máximo do intervalo deve ser maior que o valor mínimo do intervalo. Por padrão, o valor de intervalo máximo é 100.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna os valores do intervalo anterior, se for bem-sucedido, ou zero caso contrário. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo anterior e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo anterior.

## <a name="remarks"></a>Comentários

Se você não definir os valores de intervalo, o sistema definirá o valor mínimo como 0 e o valor máximo como 100. Como essa mensagem expressa o intervalo como um inteiro sem sinal de 16 bits, ele pode se estender de 0 a 65.535. O valor mínimo no intervalo pode ser de 0 a 65.535. Da mesma forma, o valor máximo pode ser de 0 a 65.535.

Para definir um intervalo maior, chame o [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetRange do PBM \_**](pbm-getrange.md)
</dt> <dt>

[**SETRANGE32 do PBM \_**](pbm-setrange32.md)
</dt> </dl>

 

