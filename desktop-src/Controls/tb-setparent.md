---
title: Mensagem de TB_SETPARENT (commctrl. h)
description: Define a janela à qual o controle Toolbar envia mensagens de notificação.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Controles de TB_SETPARENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824719"
---
# <a name="tb_setparent-message"></a>Mensagem de TB \_ SETpai

Define a janela à qual o controle Toolbar envia mensagens de notificação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Manipule a janela para receber mensagens de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um identificador para a janela de notificação anterior ou **nulo** se não houver nenhuma janela de notificação anterior.

## <a name="remarks"></a>Comentários

A mensagem de **TB \_ setpai** não altera a janela pai que foi especificada quando o controle foi criado. Chamar a função [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para um controle Toolbar retornará a janela pai real, não a janela especificada em **TB \_ setpai**. Para alterar a janela pai do controle, chame a função [**setpai**](/windows/desktop/api/winuser/nf-winuser-setparent) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

