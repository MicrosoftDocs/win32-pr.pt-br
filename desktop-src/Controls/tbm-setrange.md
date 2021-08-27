---
title: TBM_SETRANGE mensagem (Commctrl.h)
description: Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em uma barra de faixa.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE controles Windows mensagem
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061136"
---
# <a name="tbm_setrange-message"></a>Mensagem \_ TBM SETRANGE

Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em uma barra de faixa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Redesenhar sinalizador. Se esse parâmetro for **TRUE,** a barra de faixa será redesenhada depois que o intervalo for definido. Se esse parâmetro for **FALSE,** a mensagem define o intervalo, mas não redesenha a barra de faixa.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a posição mínima para o controle deslizante e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição máxima.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição do controle deslizante atual estiver fora do novo intervalo, a mensagem **\_ SETRANGE TBM** definirá a posição do controle deslizante como o novo valor máximo ou mínimo.

Como essa mensagem aceita dois valores inteiros sem sinal de 16 bits, o intervalo máximo que essa mensagem pode especificar é de 0 a 65.535. Para especificar valores de intervalo maiores, use as [**mensagens TBM \_ SETRANGEMIN**](tbm-setrangemin.md) e [**TBM \_ SETRANGEMAX.**](tbm-setrangemax.md)

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

