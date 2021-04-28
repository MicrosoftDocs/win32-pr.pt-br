---
title: Mensagem de TBM_SETPOSNOTIFY (commctrl. h)
description: TBM_SETPOSNOTIFY mensagem – define a posição lógica atual do controle deslizante em um TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Controles de TBM_SETPOSNOTIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104074"
---
# <a name="tbm_setposnotify-message"></a>\_Mensagem tbm SETPOSNOTIFY

Define a posição lógica atual do controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

wParam não utilizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova posição lógica do controle deslizante. As posições lógicas válidas são os valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante. Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Chamar **tbm \_ SETPOSNOTIFY** definirá o local do controle deslizante TrackBar como [**tbm \_ SETPOS**](tbm-setpos.md) , mas também fará com que o TrackBar Notifique seu pai de uma movimentação por meio de uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





