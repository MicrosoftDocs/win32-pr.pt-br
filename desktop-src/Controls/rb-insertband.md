---
title: Mensagem de RB_INSERTBAND (commctrl. h)
description: Insere uma nova faixa em um controle rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Controles de RB_INSERTBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824850"
---
# <a name="rb_insertband-message"></a>\_Mensagem INSERTBAND RB

Insere uma nova faixa em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero do local onde a banda será inserida. Se você definir esse parâmetro como-1, o controle adicionará a nova banda no último local.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define a banda a ser inserida. Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(REBARBANDINFO) antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





