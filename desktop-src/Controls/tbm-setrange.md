---
title: Mensagem de TBM_SETRANGE (commctrl. h)
description: Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em um TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Controles de TBM_SETRANGE de mensagens do Windows
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
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009119"
---
# <a name="tbm_setrange-message"></a>\_Mensagem SETRANGE tbm

Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, o TrackBar será redesenhado depois que o intervalo for definido. Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a posição mínima para o controle deslizante e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição máxima.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição do controle deslizante atual estiver fora do novo intervalo, a mensagem **\_ SETRANGE tbm** definirá a posição do controle deslizante como o novo valor máximo ou mínimo.

Como essa mensagem usa valores inteiros sem sinal de 2 16 bits, o intervalo máximo que essa mensagem pode especificar é de 0 a 65.535. Para especificar valores de intervalo maiores, use as mensagens [**tbm \_ SETRANGEMIN**](tbm-setrangemin.md) e [**tbm \_ SETRANGEMAX**](tbm-setrangemax.md) .

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

