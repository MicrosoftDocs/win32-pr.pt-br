---
title: Mensagem de TCM_SETCURSEL (commctrl. h)
description: Seleciona uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal TabCtrl.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Controles de TCM_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918477"
---
# <a name="tcm_setcursel-message"></a>Mensagem de TCM \_ SETcurseal

Seleciona uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da guia a ser selecionada.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da guia selecionada anteriormente, se for bem-sucedido, ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Um controle guia não envia um código de notificação [TCN \_ SELCHANGING](tcn-selchanging.md) ou [TCN \_ SELCHANGE](tcn-selchange.md) quando uma guia é selecionada usando essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





