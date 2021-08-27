---
title: Mensagem de TCM_SETCURSEL (commctrl. h)
description: Seleciona uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal TabCtrl.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- controles de Windows de mensagem de TCM_SETCURSEL
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
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104846"
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

## <a name="return-value"></a>Valor retornado

Retorna o índice da guia selecionada anteriormente, se for bem-sucedido, ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Um controle guia não envia um código de notificação [TCN \_ SELCHANGING](tcn-selchanging.md) ou [TCN \_ SELCHANGE](tcn-selchange.md) quando uma guia é selecionada usando essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





