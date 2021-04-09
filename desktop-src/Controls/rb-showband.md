---
title: Mensagem de RB_SHOWBAND (commctrl. h)
description: Mostra ou oculta uma determinada faixa em um controle rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- Controles de RB_SHOWBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086412"
---
# <a name="rb_showband-message"></a>\_Mensagem de CONBANDA RB

Mostra ou oculta uma determinada faixa em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero de uma banda no controle rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **bool** que indica se a banda deve ser mostrada ou ocultada. Se esse valor for diferente de zero, a banda será mostrada. Caso contrário, a banda ficará oculta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





