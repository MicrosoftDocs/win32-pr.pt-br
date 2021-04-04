---
title: Mensagem de ACM_ISPLAYING (commctrl. h)
description: Verifica se um clipe AVI (intercalado Audio-Video) está sendo reproduzido. Você pode enviar essa mensagem explicitamente ou usar a \_ macro de IsPlaying de animação.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Controles de ACM_ISPLAYING de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009077"
---
# <a name="acm_isplaying-message"></a>Mensagem de exibição do ACM \_

Verifica se um clipe AVI (intercalado Audio-Video) está sendo reproduzido. Você pode enviar essa mensagem explicitamente ou usar a macro de [**\_ IsPlaying de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





