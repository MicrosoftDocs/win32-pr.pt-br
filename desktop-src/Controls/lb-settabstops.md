---
title: Mensagem de LB_SETTABSTOPS (WinUser. h)
description: Define as posições de parada de tabulação em uma caixa de listagem.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Controles de LB_SETTABSTOPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824674"
---
# <a name="lb_settabstops-message"></a>Mensagem do LB \_ SETtabstops

Define as posições de parada de tabulação em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o número de paradas de tabulação.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o primeiro membro de uma matriz de inteiros contendo as paradas de tabulação. Os inteiros representam o número de trimestres da largura média de caracteres da fonte selecionada na caixa de listagem. Por exemplo, uma parada de tabulação de 4 é colocada em 1,0 unidades de caracteres e uma parada de tabulação de 6 é colocada em unidades de caracteres médias de 1,5. No entanto, se a caixa de listagem fizer parte de uma caixa de diálogo, os inteiros estarão em unidades de modelo de caixa de diálogo. As paradas de tabulação devem ser classificadas em ordem crescente; Não são permitidas guias regressivas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se todas as guias especificadas forem definidas, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="remarks"></a>Comentários

Para responder à mensagem do **lb \_ SetTabStops** , a caixa de listagem deve ter sido criada com o estilo [**lbs \_ USETABSTOPS**](list-box-styles.md) .

Se *wParam* for 0 e *lParam* for **NULL**, a parada de tabulação padrão será de duas unidades de modelo de caixa de diálogo. Se *wParam* for 1, a caixa de listagem terá paradas de tabulação separadas pela distância especificada por *lParam*.

Se *lParam* apontar para mais de um único valor, uma parada de tabulação será definida para cada valor em *lParam*, até o número especificado por *wParam*.

Os valores especificados por *lParam* estão em unidades de modelo de caixa de diálogo, que são as unidades independentes de dispositivo usadas em modelos de caixas de diálogo. Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a função [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o buffer apontado por *lParam* deve residir na memória gravável, embora a mensagem não modifique a matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

