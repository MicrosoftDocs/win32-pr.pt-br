---
title: TB_SETPARENT mensagem (Commctrl.h)
description: Define a janela para a qual o controle da barra de ferramentas envia mensagens de notificação.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT controles de Windows mensagem
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
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078140"
---
# <a name="tb_setparent-message"></a>Mensagem \_ SETPARENT de TB

Define a janela para a qual o controle da barra de ferramentas envia mensagens de notificação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com a janela para receber mensagens de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um handle para a janela de notificação anterior ou **NULL** se não houver nenhuma janela de notificação anterior.

## <a name="remarks"></a>Comentários

A **mensagem TB \_ SETPARENT** não altera a janela pai que foi especificada quando o controle foi criado. Chamar a [**função GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para um controle de barra de ferramentas retornará a janela pai real, não a janela especificada em **TB \_ SETPARENT.** Para alterar a janela pai do controle, chame a [**função SetParent.**](/windows/desktop/api/winuser/nf-winuser-setparent)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

