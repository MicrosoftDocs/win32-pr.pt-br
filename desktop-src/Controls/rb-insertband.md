---
title: Mensagem de RB_INSERTBAND (commctrl. h)
description: Insere uma nova faixa em um controle rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- controles de Windows de mensagem de RB_INSERTBAND
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
ms.openlocfilehash: e0e21020302e4dcbfeb75f4a57d37be4b5c5703668231e8ec8e9dd9bd9577cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770156"
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

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





