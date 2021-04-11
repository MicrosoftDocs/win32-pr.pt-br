---
title: Mensagem de RB_GETRECT (commctrl. h)
description: Recupera o retângulo delimitador para uma determinada faixa em um controle rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Controles de RB_GETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163598"
---
# <a name="rb_getrect-message"></a>\_Mensagem de GETRECT RB

Recupera o retângulo delimitador para uma determinada faixa em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero de uma banda no controle rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá os limites da faixa Rebar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

