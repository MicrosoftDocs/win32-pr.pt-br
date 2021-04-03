---
title: Mensagem de RB_GETBANDBORDERS (commctrl. h)
description: Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área utilizável em uma banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Controles de RB_GETBANDBORDERS de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918781"
---
# <a name="rb_getbandborders-message"></a>\_Mensagem GETBANDBORDERS RB

Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área utilizável em uma banda.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda para a qual as bordas serão recuperadas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as bordas da faixa. Se o controle rebar tiver o estilo [**RBS \_ BANDBORDERS**](rebar-control-styles.md) , cada membro dessa estrutura receberá o número de pixels, no lado correspondente da faixa, que constitui a borda. Se o controle rebar não tiver o estilo **RBS \_ BANDBORDERS** , somente o membro **à esquerda** dessa estrutura receberá informações válidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

